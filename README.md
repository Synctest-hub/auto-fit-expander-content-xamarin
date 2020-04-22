# How to autofit the Expander content in Xamarin.Forms (SfExpander)

You can resize the [SfExpander](https://help.syncfusion.com/xamarin/expander/getting-started?) [Content](https://help.syncfusion.com/cr/cref_files/xamarin/Syncfusion.Expander.XForms~Syncfusion.XForms.Expander.SfExpander~Content.html?) based on the content size by using [DynamicSizeMode](https://help.syncfusion.com/cr/xamarin/Syncfusion.Expander.XForms~Syncfusion.XForms.Expander.DynamicSizeMode.html?) as **Content** in Xamarin.Forms.

You can also refer the following article.

https://www.syncfusion.com/kb/11431/how-to-autofit-the-expander-content-in-xamarin-forms-sfexpander

**XAML**

Added [Editor](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/user-interface/text/editor) control to Expander content and set **DynamicSizeMode** to Content. To change the content size based on the text, set [AutoSize](https://docs.microsoft.com/en-us/dotnet/api/xamarin.forms.editor.autosize#Xamarin_Forms_Editor_AutoSize) as [TextChanges](https://docs.microsoft.com/en-us/dotnet/api/xamarin.forms.editorautosizeoption#Xamarin_Forms_EditorAutoSizeOption_TextChanges) for **Editor** control.
``` xml
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:local="clr-namespace:ExpanderXamarin"
             xmlns:syncfusion="clr-namespace:Syncfusion.XForms.Expander;assembly=Syncfusion.Expander.XForms"
             x:Class="ExpanderXamarin.MainPage">
    <ContentPage.Content>
        <ScrollView BackgroundColor="#EDF2F5">
            <StackLayout>
                <syncfusion:SfExpander DynamicSizeMode="Content" IsExpanded="True">
                    <syncfusion:SfExpander.Header>
                        <Grid HeightRequest="50">
                            <Label Text="Veggie burger" VerticalTextAlignment="Center"/>
                        </Grid>
                    </syncfusion:SfExpander.Header>
 
                    <syncfusion:SfExpander.Content>
                        <Grid>
                            <Editor AutoSize="TextChanges" Text="Veggie burger, garden burger, or tofu burger uses a meat analogue, a meat substitute such as tofu, textured vegetable protein, seitan (wheat gluten), Quorn, beans, grains or an assortment of vegetables, which are ground up and formed into patties."/>
                        </Grid>
                    </syncfusion:SfExpander.Content>
                </syncfusion:SfExpander>
            </StackLayout>
        </ScrollView>
    </ContentPage.Content>
</ContentPage>
```
**Output**

![AutoFitExpandeContent](https://github.com/SyncfusionExamples/auto-fit-expander-content-xamarin/blob/master/ScreenShots/AutoFitExpanderContent.gif)

# alpaca-template
here is simple example using template to change arrays control format

"fields": {
	"/myArrayName": {
		"templates": {
			"container-array-item": "<div style='border-bottom: 1px solid #ddd;padding-bottom: 10px;padding-top: 10px;'>{{#compare actionbarStyle 'top'}} {{#arrayActionbar}}{{/arrayActionbar}} {{/compare}} {{#itemField}}{{/itemField}} {{#compare actionbarStyle 'bottom'}} {{#arrayActionbar}}{{/arrayActionbar}} {{/compare}} </div>"
		}
	},
	"/myArrayName/myArrayControlName": {
		"templates": {
			"control-text": "<input style='margin-left: 50px !important;width: 290px !important;margin-top: -6px;' type='{{inputType}}' id='{{id}}' {{#if options.placeholder}}placeholder='{{options.placeholder}}'{{/if}} {{#if options.size}}size='{{options.size}}'{{/if}} {{#if options.readonly}}readonly='readonly'{{/if}} {{#if name}}name='{{name}}'{{/if}} {{#each options.data}}data-{{@key}}='{{this}}'{{/each}} {{#each options.attributes}}{{@key}}='{{this}}'{{/each}}/>{{#if options.helper}}<p class='{{#if options.helperClass}} {{options.helperClass}}{{/if}}'><i class='info-sign'></i>{{{options.helper}}}</p>{{/if}}",
		"control":"<div style='width: 50%;float: left;'>{{#if options.label}}<label style='font-weight: normal;' class='{{#if options.labelClass}} {{options.labelClass}}{{/if}} alpaca-control-label' for='{{id}}'>{{{options.label}}}</label>{{/if}} {{#control}}{{/control}}</div>"
		}
	}
}

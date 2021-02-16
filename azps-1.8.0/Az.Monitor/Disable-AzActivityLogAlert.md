---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: aba56e21b087971fc9cae6854111ef9ca4a2dc3c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403341"
---
# <span data-ttu-id="21624-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21624-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="21624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21624-102">SYNOPSIS</span></span>
<span data-ttu-id="21624-103">Disabilita un avviso del log attività e ne imposta i tag.</span><span class="sxs-lookup"><span data-stu-id="21624-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="21624-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21624-104">SYNTAX</span></span>

### <span data-ttu-id="21624-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21624-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21624-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="21624-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21624-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="21624-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21624-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21624-108">DESCRIPTION</span></span>
<span data-ttu-id="21624-109">Il cmdlet **Disable-AzActivityLogAlert** disabilita e invia un avviso nel log attività e ne consente l'impostazione dei tag.</span><span class="sxs-lookup"><span data-stu-id="21624-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="21624-110">Questo cmdlet implementa il modello ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di applicare effettivamente le patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="21624-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="21624-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21624-111">EXAMPLES</span></span>

### <span data-ttu-id="21624-112">Esempio 1: Disabilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="21624-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="21624-113">Questo comando disabilita l'avviso del log attività denominato avviso1 nel gruppo di risorse Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="21624-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="21624-114">Questo comando modifica la proprietà tag dell'avviso del log attività denominato avviso1 e lo disabilita.</span><span class="sxs-lookup"><span data-stu-id="21624-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="21624-115">Esempio 2: Disabilitare un avviso del log attività usando un oggetto PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="21624-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="21624-116">Questo comando disabilita un avviso del log attività denominato avviso1.</span><span class="sxs-lookup"><span data-stu-id="21624-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="21624-117">A questo scopo usa un oggetto PSActivityLogAlertResource come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="21624-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="21624-118">Esempio 3: Disabilitare ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="21624-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="21624-119">Questo comando disabilita ActivityLogAlert usando il parametro ResourceId dalla barra verticale.</span><span class="sxs-lookup"><span data-stu-id="21624-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="21624-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21624-120">PARAMETERS</span></span>

### <span data-ttu-id="21624-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21624-121">-DefaultProfile</span></span>
<span data-ttu-id="21624-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="21624-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21624-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21624-123">-InputObject</span></span>
<span data-ttu-id="21624-124">Imposta la proprietà tag InputObject della chiamata per estrarre il nome richiesto, il nome del gruppo di risorse e le proprietà del tag facoltative.</span><span class="sxs-lookup"><span data-stu-id="21624-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21624-125">-Name</span><span class="sxs-lookup"><span data-stu-id="21624-125">-Name</span></span>
<span data-ttu-id="21624-126">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="21624-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21624-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21624-127">-ResourceGroupName</span></span>
<span data-ttu-id="21624-128">Nome del gruppo di risorse in cui si trova la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="21624-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21624-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21624-129">-ResourceId</span></span>
<span data-ttu-id="21624-130">Imposta la proprietà tag ResourceId della chiamata per estrarre il nome richiesto e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21624-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21624-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21624-131">-Confirm</span></span>
<span data-ttu-id="21624-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21624-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21624-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21624-133">-WhatIf</span></span>
<span data-ttu-id="21624-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21624-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21624-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21624-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21624-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21624-136">CommonParameters</span></span>
<span data-ttu-id="21624-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21624-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21624-138">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21624-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21624-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="21624-139">INPUTS</span></span>

### <span data-ttu-id="21624-140">System.String</span><span class="sxs-lookup"><span data-stu-id="21624-140">System.String</span></span>

### <span data-ttu-id="21624-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="21624-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="21624-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21624-142">OUTPUTS</span></span>

### <span data-ttu-id="21624-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="21624-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="21624-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="21624-144">NOTES</span></span>

## <span data-ttu-id="21624-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21624-145">RELATED LINKS</span></span>

[<span data-ttu-id="21624-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21624-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="21624-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21624-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="21624-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21624-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="21624-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="21624-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



[<span data-ttu-id="21624-150">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="21624-150">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

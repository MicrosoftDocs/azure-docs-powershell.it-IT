---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 9d1cd1b13a24c2b5a5374d29cfd38273caa92e33
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403018"
---
# <span data-ttu-id="f409c-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f409c-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="f409c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f409c-102">SYNOPSIS</span></span>
<span data-ttu-id="f409c-103">Rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="f409c-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="f409c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f409c-104">SYNTAX</span></span>

### <span data-ttu-id="f409c-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f409c-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f409c-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f409c-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f409c-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="f409c-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f409c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f409c-108">DESCRIPTION</span></span>
<span data-ttu-id="f409c-109">Il cmdlet **Remove-AzActivityLogAlert** rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="f409c-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="f409c-110">Questo cmdlet implementa il modello ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di applicare effettivamente le patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="f409c-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="f409c-111">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f409c-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f409c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f409c-112">EXAMPLES</span></span>

### <span data-ttu-id="f409c-113">Esempio 1: Rimuovere un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="f409c-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="f409c-114">Rimuove un avviso del log attività usando come input il nome e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f409c-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="f409c-115">Esempio 2: Rimuovere un avviso del log attività usando psActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="f409c-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="f409c-116">Rimuove un avviso del log attività usando psActivityLogAlertResource come input.</span><span class="sxs-lookup"><span data-stu-id="f409c-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="f409c-117">Esempio 3: Rimuovere ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="f409c-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="f409c-118">Questo comando rimuove ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="f409c-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="f409c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f409c-119">PARAMETERS</span></span>

### <span data-ttu-id="f409c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f409c-120">-DefaultProfile</span></span>
<span data-ttu-id="f409c-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f409c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f409c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f409c-122">-InputObject</span></span>
<span data-ttu-id="f409c-123">Imposta la proprietà tag InputObject della chiamata per estrarre il nome richiesto e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f409c-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f409c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f409c-124">-Name</span></span>
<span data-ttu-id="f409c-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="f409c-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f409c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f409c-126">-ResourceGroupName</span></span>
<span data-ttu-id="f409c-127">Nome del gruppo di risorse in cui si trova la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="f409c-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f409c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f409c-128">-ResourceId</span></span>
<span data-ttu-id="f409c-129">Imposta la proprietà tag ResourceId della chiamata per estrarre il nome richiesto e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f409c-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f409c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f409c-130">-Confirm</span></span>
<span data-ttu-id="f409c-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f409c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f409c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f409c-132">-WhatIf</span></span>
<span data-ttu-id="f409c-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f409c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f409c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f409c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f409c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f409c-135">CommonParameters</span></span>
<span data-ttu-id="f409c-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f409c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f409c-137">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f409c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f409c-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="f409c-138">INPUTS</span></span>

### <span data-ttu-id="f409c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f409c-139">System.String</span></span>

### <span data-ttu-id="f409c-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="f409c-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="f409c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f409c-141">OUTPUTS</span></span>

### <span data-ttu-id="f409c-142">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f409c-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="f409c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="f409c-143">NOTES</span></span>

## <span data-ttu-id="f409c-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f409c-144">RELATED LINKS</span></span>

[<span data-ttu-id="f409c-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f409c-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="f409c-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f409c-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="f409c-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f409c-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="f409c-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f409c-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="f409c-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f409c-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)




---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: aff7540a11df1da5922c9bf2f9817309c3157365
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032445"
---
# <span data-ttu-id="72c13-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72c13-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="72c13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72c13-102">SYNOPSIS</span></span>
<span data-ttu-id="72c13-103">Rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="72c13-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="72c13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72c13-104">SYNTAX</span></span>

### <span data-ttu-id="72c13-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72c13-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c13-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="72c13-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72c13-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="72c13-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72c13-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72c13-108">DESCRIPTION</span></span>
<span data-ttu-id="72c13-109">Il cmdlet **Remove-AzActivityLogAlert** rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="72c13-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="72c13-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="72c13-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="72c13-111">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="72c13-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="72c13-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72c13-112">EXAMPLES</span></span>

### <span data-ttu-id="72c13-113">Esempio 1: rimuovere un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="72c13-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="72c13-114">Rimuove un avviso del log attività usando il nome e il nome del gruppo di risorse come input.</span><span class="sxs-lookup"><span data-stu-id="72c13-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="72c13-115">Esempio 2: rimuovere un avviso del log attività usando un PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="72c13-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="72c13-116">Rimuove un avviso del log attività usando un PSActivityLogAlertResource come input.</span><span class="sxs-lookup"><span data-stu-id="72c13-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="72c13-117">Esempio 3: rimuovere il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c13-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="72c13-118">Questo comando rimuove ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="72c13-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="72c13-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72c13-119">PARAMETERS</span></span>

### <span data-ttu-id="72c13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c13-120">-DefaultProfile</span></span>
<span data-ttu-id="72c13-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="72c13-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72c13-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72c13-122">-InputObject</span></span>
<span data-ttu-id="72c13-123">Imposta la proprietà InputObject tag della chiamata per estrarre il nome obbligatorio e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72c13-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="72c13-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="72c13-124">-Name</span></span>
<span data-ttu-id="72c13-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="72c13-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="72c13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c13-126">-ResourceGroupName</span></span>
<span data-ttu-id="72c13-127">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="72c13-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="72c13-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c13-128">-ResourceId</span></span>
<span data-ttu-id="72c13-129">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="72c13-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="72c13-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72c13-130">-Confirm</span></span>
<span data-ttu-id="72c13-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72c13-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72c13-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72c13-132">-WhatIf</span></span>
<span data-ttu-id="72c13-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72c13-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72c13-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72c13-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72c13-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c13-135">CommonParameters</span></span>
<span data-ttu-id="72c13-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c13-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c13-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72c13-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c13-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72c13-138">INPUTS</span></span>

### <span data-ttu-id="72c13-139">System. String</span><span class="sxs-lookup"><span data-stu-id="72c13-139">System.String</span></span>

### <span data-ttu-id="72c13-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="72c13-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="72c13-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72c13-141">OUTPUTS</span></span>

### <span data-ttu-id="72c13-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="72c13-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="72c13-143">Note</span><span class="sxs-lookup"><span data-stu-id="72c13-143">NOTES</span></span>

## <span data-ttu-id="72c13-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72c13-144">RELATED LINKS</span></span>

[<span data-ttu-id="72c13-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72c13-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="72c13-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72c13-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="72c13-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72c13-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="72c13-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72c13-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="72c13-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="72c13-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="72c13-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="72c13-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)


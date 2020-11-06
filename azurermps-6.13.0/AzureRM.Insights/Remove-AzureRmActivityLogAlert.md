---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: 8749744d6ab10ba1b48f7c8e56792c5891edb5eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510987"
---
# <span data-ttu-id="5a83d-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5a83d-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="5a83d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a83d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a83d-103">Rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="5a83d-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a83d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a83d-104">SYNTAX</span></span>

### <span data-ttu-id="5a83d-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a83d-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a83d-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a83d-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a83d-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a83d-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a83d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a83d-108">DESCRIPTION</span></span>
<span data-ttu-id="5a83d-109">Il cmdlet **Remove-AzureRmActivityLogAlert** rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="5a83d-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="5a83d-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a83d-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="5a83d-111">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a83d-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5a83d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a83d-112">EXAMPLES</span></span>

### <span data-ttu-id="5a83d-113">Esempio 1: rimuovere un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="5a83d-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="5a83d-114">Rimuove un avviso del log attività usando il nome e il nome del gruppo di risorse come input.</span><span class="sxs-lookup"><span data-stu-id="5a83d-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="5a83d-115">Esempio 2: rimuovere un avviso del log attività usando un PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="5a83d-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="5a83d-116">Rimuove un avviso del log attività usando un PSActivityLogAlertResource come input.</span><span class="sxs-lookup"><span data-stu-id="5a83d-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="5a83d-117">Esempio 3: rimuovere il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a83d-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="5a83d-118">Questo comando rimuove ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="5a83d-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="5a83d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a83d-119">PARAMETERS</span></span>

### <span data-ttu-id="5a83d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a83d-120">-DefaultProfile</span></span>
<span data-ttu-id="5a83d-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5a83d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a83d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a83d-122">-InputObject</span></span>
<span data-ttu-id="5a83d-123">Imposta la proprietà InputObject tag della chiamata per estrarre il nome obbligatorio e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5a83d-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="5a83d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a83d-124">-Name</span></span>
<span data-ttu-id="5a83d-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="5a83d-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="5a83d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a83d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a83d-127">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="5a83d-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="5a83d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a83d-128">-ResourceId</span></span>
<span data-ttu-id="5a83d-129">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="5a83d-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="5a83d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a83d-130">-Confirm</span></span>
<span data-ttu-id="5a83d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a83d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a83d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a83d-132">-WhatIf</span></span>
<span data-ttu-id="5a83d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a83d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a83d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a83d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a83d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a83d-135">CommonParameters</span></span>
<span data-ttu-id="5a83d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a83d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a83d-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a83d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a83d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a83d-138">INPUTS</span></span>

### <span data-ttu-id="5a83d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5a83d-139">System.String</span></span>

### <span data-ttu-id="5a83d-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="5a83d-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="5a83d-141">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a83d-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5a83d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a83d-142">OUTPUTS</span></span>

### <span data-ttu-id="5a83d-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5a83d-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5a83d-144">Note</span><span class="sxs-lookup"><span data-stu-id="5a83d-144">NOTES</span></span>

## <span data-ttu-id="5a83d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a83d-145">RELATED LINKS</span></span>

[<span data-ttu-id="5a83d-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5a83d-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5a83d-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5a83d-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5a83d-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5a83d-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5a83d-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5a83d-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5a83d-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="5a83d-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="5a83d-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5a83d-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


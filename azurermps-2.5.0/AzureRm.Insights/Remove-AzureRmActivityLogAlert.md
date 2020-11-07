---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 1dfd435d2797ee7430349546a5d2ba6fa2fe0023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866345"
---
# <span data-ttu-id="84849-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84849-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="84849-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84849-102">SYNOPSIS</span></span>
<span data-ttu-id="84849-103">Rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="84849-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84849-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84849-104">SYNTAX</span></span>

### <span data-ttu-id="84849-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="84849-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84849-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="84849-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84849-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="84849-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84849-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84849-108">DESCRIPTION</span></span>
<span data-ttu-id="84849-109">Il cmdlet **Remove-AzureRmActivityLogAlert** rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="84849-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="84849-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="84849-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="84849-111">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="84849-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="84849-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84849-112">EXAMPLES</span></span>

### <span data-ttu-id="84849-113">Esempio 1: rimuovere un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="84849-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="84849-114">Rimuove un avviso del log attività usando il nome e il nome del gruppo di risorse come input.</span><span class="sxs-lookup"><span data-stu-id="84849-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="84849-115">Esempio 2: rimuovere un avviso del log attività usando un PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="84849-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="84849-116">Rimuove un avviso del log attività usando un PSActivityLogAlertResource come input.</span><span class="sxs-lookup"><span data-stu-id="84849-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="84849-117">Esempio 3: rimuovere il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="84849-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="84849-118">Questo comando rimuove ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="84849-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="84849-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84849-119">PARAMETERS</span></span>

### <span data-ttu-id="84849-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84849-120">-DefaultProfile</span></span>
<span data-ttu-id="84849-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="84849-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84849-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84849-122">-InputObject</span></span>
<span data-ttu-id="84849-123">Imposta la proprietà InputObject tag della chiamata per estrarre il nome obbligatorio e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84849-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="84849-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="84849-124">-Name</span></span>
<span data-ttu-id="84849-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="84849-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="84849-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84849-126">-ResourceGroupName</span></span>
<span data-ttu-id="84849-127">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="84849-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="84849-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84849-128">-ResourceId</span></span>
<span data-ttu-id="84849-129">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="84849-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="84849-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84849-130">-Confirm</span></span>
<span data-ttu-id="84849-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84849-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84849-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84849-132">-WhatIf</span></span>
<span data-ttu-id="84849-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84849-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84849-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84849-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84849-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84849-135">CommonParameters</span></span>
<span data-ttu-id="84849-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84849-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84849-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84849-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84849-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84849-138">INPUTS</span></span>

### <span data-ttu-id="84849-139">System. String</span><span class="sxs-lookup"><span data-stu-id="84849-139">System.String</span></span>

### <span data-ttu-id="84849-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="84849-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="84849-141">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="84849-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="84849-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84849-142">OUTPUTS</span></span>

### <span data-ttu-id="84849-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="84849-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="84849-144">Note</span><span class="sxs-lookup"><span data-stu-id="84849-144">NOTES</span></span>

## <span data-ttu-id="84849-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84849-145">RELATED LINKS</span></span>

[<span data-ttu-id="84849-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84849-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="84849-147">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84849-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="84849-148">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84849-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="84849-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="84849-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="84849-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="84849-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="84849-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="84849-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


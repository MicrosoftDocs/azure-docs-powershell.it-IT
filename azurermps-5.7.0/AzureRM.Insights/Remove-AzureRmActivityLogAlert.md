---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: b712363b2b4e1d610f00f1111c48145debe084a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519455"
---
# <span data-ttu-id="79ebc-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="79ebc-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="79ebc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="79ebc-103">Rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="79ebc-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79ebc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79ebc-104">SYNTAX</span></span>

### <span data-ttu-id="79ebc-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="79ebc-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79ebc-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="79ebc-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79ebc-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="79ebc-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79ebc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79ebc-108">DESCRIPTION</span></span>
<span data-ttu-id="79ebc-109">Il cmdlet **Remove-AzureRmActivityLogAlert** rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="79ebc-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="79ebc-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="79ebc-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

<span data-ttu-id="79ebc-111">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="79ebc-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="79ebc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79ebc-112">EXAMPLES</span></span>

### <span data-ttu-id="79ebc-113">Esempio 1: rimuovere un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="79ebc-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="79ebc-114">Rimuove un avviso del log attività usando il nome e il nome del gruppo di risorse come input.</span><span class="sxs-lookup"><span data-stu-id="79ebc-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="79ebc-115">Esempio 2: rimuovere un avviso del log attività usando un PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="79ebc-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="79ebc-116">Rimuove un avviso del log attività usando un PSActivityLogAlertResource come input.</span><span class="sxs-lookup"><span data-stu-id="79ebc-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="79ebc-117">Esempio 3: rimuovere il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="79ebc-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="79ebc-118">Questo comando rimuove ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="79ebc-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="79ebc-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79ebc-119">PARAMETERS</span></span>

### <span data-ttu-id="79ebc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ebc-120">-DefaultProfile</span></span>
<span data-ttu-id="79ebc-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="79ebc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ebc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79ebc-122">-InputObject</span></span>
<span data-ttu-id="79ebc-123">Imposta la proprietà InputObject tag della chiamata per estrarre il nome obbligatorio e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79ebc-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79ebc-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="79ebc-124">-Name</span></span>
<span data-ttu-id="79ebc-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="79ebc-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ebc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ebc-126">-ResourceGroupName</span></span>
<span data-ttu-id="79ebc-127">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="79ebc-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ebc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79ebc-128">-ResourceId</span></span>
<span data-ttu-id="79ebc-129">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="79ebc-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79ebc-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79ebc-130">-Confirm</span></span>
<span data-ttu-id="79ebc-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79ebc-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ebc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79ebc-132">-WhatIf</span></span>
<span data-ttu-id="79ebc-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79ebc-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79ebc-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79ebc-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ebc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ebc-135">CommonParameters</span></span>
<span data-ttu-id="79ebc-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79ebc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ebc-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ebc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ebc-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79ebc-138">INPUTS</span></span>

### <span data-ttu-id="79ebc-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79ebc-139">None</span></span>
<span data-ttu-id="79ebc-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="79ebc-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79ebc-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79ebc-141">OUTPUTS</span></span>

### <span data-ttu-id="79ebc-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="79ebc-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="79ebc-143">Note</span><span class="sxs-lookup"><span data-stu-id="79ebc-143">NOTES</span></span>

## <span data-ttu-id="79ebc-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79ebc-144">RELATED LINKS</span></span>

[<span data-ttu-id="79ebc-145">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="79ebc-145">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="79ebc-146">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="79ebc-146">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="79ebc-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="79ebc-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="79ebc-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="79ebc-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="79ebc-149">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="79ebc-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="79ebc-150">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="79ebc-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


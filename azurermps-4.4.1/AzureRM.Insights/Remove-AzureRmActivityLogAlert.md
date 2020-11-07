---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688636"
---
# <span data-ttu-id="5f9f7-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5f9f7-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="5f9f7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f9f7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9f7-103">Rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f9f7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f9f7-104">SYNTAX</span></span>

### <span data-ttu-id="5f9f7-105">Parametri predefiniti per la rimozione di un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="5f9f7-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f9f7-106">Parametri per rimuovere gli avvisi del log attività che prendono valore dalla pipe</span><span class="sxs-lookup"><span data-stu-id="5f9f7-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f9f7-107">Parametri per la rimozione di avvisi del log attività che impiegano il valore di ResourceId dalla pipe</span><span class="sxs-lookup"><span data-stu-id="5f9f7-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f9f7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f9f7-108">DESCRIPTION</span></span>
<span data-ttu-id="5f9f7-109">Il cmdlet **Remove-AzureRmActivityLogAlert** rimuove un avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="5f9f7-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="5f9f7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f9f7-111">EXAMPLES</span></span>

### <span data-ttu-id="5f9f7-112">Esempio 1: rimuovere un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="5f9f7-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="5f9f7-113">Rimuove un avviso del log attività usando il nome e il nome del gruppo di risorse come input.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="5f9f7-114">Esempio 2: rimuovere un avviso del log attività usando un PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="5f9f7-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="5f9f7-115">Rimuove un avviso del log attività usando un PSActivityLogAlertResource come input.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="5f9f7-116">Esempio 3: rimuovere il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f9f7-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="5f9f7-117">Questo comando rimuove ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="5f9f7-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f9f7-118">PARAMETERS</span></span>

### <span data-ttu-id="5f9f7-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f9f7-119">-Name</span></span>
<span data-ttu-id="5f9f7-120">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9f7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f9f7-121">-ResourceGroupName</span></span>
<span data-ttu-id="5f9f7-122">Nome del gruppo di risorse in cui è presente la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9f7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f9f7-123">-InputObject</span></span>
<span data-ttu-id="5f9f7-124">Imposta la proprietà InputObject tag della chiamata per estrarre il nome obbligatorio e le proprietà del nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9f7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f9f7-125">-ResourceId</span></span>
<span data-ttu-id="5f9f7-126">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9f7-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f9f7-127">-Confirm</span></span>
<span data-ttu-id="5f9f7-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f9f7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9f7-129">-DefaultProfile</span></span>
<span data-ttu-id="5f9f7-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f9f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f9f7-131">-WhatIf</span></span>
<span data-ttu-id="5f9f7-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f9f7-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f9f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9f7-134">CommonParameters</span></span>
<span data-ttu-id="5f9f7-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f9f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9f7-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f9f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9f7-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f9f7-137">INPUTS</span></span>

## <span data-ttu-id="5f9f7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f9f7-138">OUTPUTS</span></span>

### <span data-ttu-id="5f9f7-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5f9f7-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5f9f7-140">Note</span><span class="sxs-lookup"><span data-stu-id="5f9f7-140">NOTES</span></span>

## <span data-ttu-id="5f9f7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f9f7-141">RELATED LINKS</span></span>

[<span data-ttu-id="5f9f7-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5f9f7-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5f9f7-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5f9f7-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5f9f7-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5f9f7-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5f9f7-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5f9f7-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5f9f7-146">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="5f9f7-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="5f9f7-147">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5f9f7-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


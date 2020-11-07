---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: cf920fe8fbe235a2c003bebc0cdecf1a480926ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688291"
---
# <span data-ttu-id="a9f8a-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a9f8a-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="a9f8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f8a-103">Disabilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9f8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9f8a-104">SYNTAX</span></span>

### <span data-ttu-id="a9f8a-105">Parametri predefiniti per disabilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="a9f8a-105">Default parameters for disable an activity log alert</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9f8a-106">Parametri per disabilitare gli avvisi del log attività che prendono valore dalla pipe</span><span class="sxs-lookup"><span data-stu-id="a9f8a-106">Parameters to disable an activity log alerts taking value from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9f8a-107">Parametri per disabilitare gli avvisi di un log delle attività che impiegano il valore di ResourceId dalla pipe</span><span class="sxs-lookup"><span data-stu-id="a9f8a-107">Parameters to disable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9f8a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9f8a-108">DESCRIPTION</span></span>
<span data-ttu-id="a9f8a-109">Il cmdlet **Disable-AzureRmActivityLogAlert disattiva** l'avviso e il log delle attività e consente di impostare i relativi contrassegni.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="a9f8a-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a9f8a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9f8a-111">EXAMPLES</span></span>

### <span data-ttu-id="a9f8a-112">Esempio 1: disabilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="a9f8a-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="a9f8a-113">Questo comando Disabilita l'avviso del log attività denominato Alert1 nel gruppo di risorse predefinito-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

<span data-ttu-id="a9f8a-114">Questo comando modifica la proprietà Tags dell'avviso del log attività denominato Alert1 e lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="a9f8a-115">Esempio 2: disabilitare un avviso del log attività usando un oggetto PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="a9f8a-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="a9f8a-116">Questo comando Disabilita un avviso del log attività denominato Alert1.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="a9f8a-117">Per questo usa un oggetto PSActivityLogAlertResource come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="a9f8a-118">Esempio 3: disabilitare il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f8a-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="a9f8a-119">Questo comando Disabilita ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a9f8a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9f8a-120">PARAMETERS</span></span>

### <span data-ttu-id="a9f8a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9f8a-121">-Name</span></span>
<span data-ttu-id="a9f8a-122">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-122">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f8a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f8a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9f8a-124">Nome del gruppo di risorse in cui sta per esistere la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-124">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f8a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9f8a-125">-InputObject</span></span>
<span data-ttu-id="a9f8a-126">Imposta la proprietà InputObject tag della chiamata per estrarre il nome necessario, il nome del gruppo di risorse e le proprietà facoltative del tag.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-126">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to disable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f8a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f8a-127">-ResourceId</span></span>
<span data-ttu-id="a9f8a-128">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-128">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to disable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9f8a-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9f8a-129">-Confirm</span></span>
<span data-ttu-id="a9f8a-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9f8a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f8a-131">-DefaultProfile</span></span>
<span data-ttu-id="a9f8a-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9f8a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9f8a-133">-WhatIf</span></span>
<span data-ttu-id="a9f8a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9f8a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9f8a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f8a-136">CommonParameters</span></span>
<span data-ttu-id="a9f8a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f8a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f8a-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f8a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f8a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9f8a-139">INPUTS</span></span>

## <span data-ttu-id="a9f8a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9f8a-140">OUTPUTS</span></span>

### <span data-ttu-id="a9f8a-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a9f8a-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a9f8a-142">Note</span><span class="sxs-lookup"><span data-stu-id="a9f8a-142">NOTES</span></span>

## <span data-ttu-id="a9f8a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9f8a-143">RELATED LINKS</span></span>

[<span data-ttu-id="a9f8a-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a9f8a-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a9f8a-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a9f8a-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a9f8a-146">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a9f8a-146">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="a9f8a-147">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a9f8a-147">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="a9f8a-148">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a9f8a-148">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="a9f8a-149">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a9f8a-149">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

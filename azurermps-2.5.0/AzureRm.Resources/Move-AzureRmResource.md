---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
ms.openlocfilehash: 4f50aea600fe930de62a65d566b6a6ec723fc8de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866637"
---
# <span data-ttu-id="92a1f-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="92a1f-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="92a1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="92a1f-103">Sposta una risorsa in un gruppo o un abbonamento di risorse diverso.</span><span class="sxs-lookup"><span data-stu-id="92a1f-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92a1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92a1f-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92a1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="92a1f-106">Il cmdlet **Move-AzureRmResource** sposta le risorse esistenti in un gruppo di risorse diverso.</span><span class="sxs-lookup"><span data-stu-id="92a1f-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="92a1f-107">Il gruppo di risorse può avere un abbonamento diverso.</span><span class="sxs-lookup"><span data-stu-id="92a1f-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="92a1f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92a1f-108">EXAMPLES</span></span>

### <span data-ttu-id="92a1f-109">Esempio 1: trasferire una risorsa in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="92a1f-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="92a1f-110">Con il primo comando viene ottenuta una risorsa denominata ContosoStorageAccount tramite il cmdlet Get-AzureRmResource e la risorsa viene archiviata nella variabile $Resource.</span><span class="sxs-lookup"><span data-stu-id="92a1f-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="92a1f-111">Il secondo comando Sposta la risorsa nel gruppo di risorse denominato ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="92a1f-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="92a1f-112">Il comando identifica la risorsa per lo stato di trasferimento tramite la proprietà **resourceId** di $Resource.</span><span class="sxs-lookup"><span data-stu-id="92a1f-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="92a1f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92a1f-113">PARAMETERS</span></span>

### <span data-ttu-id="92a1f-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="92a1f-114">-ApiVersion</span></span>
<span data-ttu-id="92a1f-115">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="92a1f-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="92a1f-116">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="92a1f-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a1f-117">-DefaultProfile</span></span>
<span data-ttu-id="92a1f-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="92a1f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92a1f-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a1f-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="92a1f-120">Specifica il nome del gruppo di risorse in cui questo cmdlet sposta le risorse.</span><span class="sxs-lookup"><span data-stu-id="92a1f-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92a1f-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="92a1f-122">Specifica l'ID della sottoscrizione in cui questo cmdlet sposta le risorse.</span><span class="sxs-lookup"><span data-stu-id="92a1f-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="92a1f-123">-Force</span></span>
<span data-ttu-id="92a1f-124">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="92a1f-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="92a1f-125">-InformationAction</span></span>
<span data-ttu-id="92a1f-126">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="92a1f-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="92a1f-127">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="92a1f-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92a1f-128">Continuare</span><span class="sxs-lookup"><span data-stu-id="92a1f-128">Continue</span></span>
- <span data-ttu-id="92a1f-129">Ignora</span><span class="sxs-lookup"><span data-stu-id="92a1f-129">Ignore</span></span>
- <span data-ttu-id="92a1f-130">Informarsi</span><span class="sxs-lookup"><span data-stu-id="92a1f-130">Inquire</span></span>
- <span data-ttu-id="92a1f-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="92a1f-131">SilentlyContinue</span></span>
- <span data-ttu-id="92a1f-132">Stop</span><span class="sxs-lookup"><span data-stu-id="92a1f-132">Stop</span></span>
- <span data-ttu-id="92a1f-133">Sospensione</span><span class="sxs-lookup"><span data-stu-id="92a1f-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="92a1f-134">-InformationVariable</span></span>
<span data-ttu-id="92a1f-135">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="92a1f-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="92a1f-136">-Pre</span></span>
<span data-ttu-id="92a1f-137">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="92a1f-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92a1f-138">-ResourceId</span></span>
<span data-ttu-id="92a1f-139">Specifica una matrice di ID delle risorse spostate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a1f-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="92a1f-140">-Confirm</span></span>
<span data-ttu-id="92a1f-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92a1f-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a1f-142">-WhatIf</span></span>
<span data-ttu-id="92a1f-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a1f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a1f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="92a1f-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a1f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a1f-145">CommonParameters</span></span>
<span data-ttu-id="92a1f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a1f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a1f-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a1f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a1f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92a1f-148">INPUTS</span></span>

## <span data-ttu-id="92a1f-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92a1f-149">OUTPUTS</span></span>

## <span data-ttu-id="92a1f-150">Note</span><span class="sxs-lookup"><span data-stu-id="92a1f-150">NOTES</span></span>

## <span data-ttu-id="92a1f-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92a1f-151">RELATED LINKS</span></span>



[<span data-ttu-id="92a1f-152">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="92a1f-152">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="92a1f-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="92a1f-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="92a1f-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="92a1f-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="92a1f-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="92a1f-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)



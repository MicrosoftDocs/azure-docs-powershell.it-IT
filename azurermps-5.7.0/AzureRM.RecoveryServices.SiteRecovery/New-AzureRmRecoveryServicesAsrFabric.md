---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 53398a882ff513443f8eae336539858f7fe34ce4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518048"
---
# <span data-ttu-id="79a35-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="79a35-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="79a35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79a35-102">SYNOPSIS</span></span>
<span data-ttu-id="79a35-103">Crea un tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="79a35-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79a35-104">SYNTAX</span></span>

### <span data-ttu-id="79a35-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79a35-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a35-106">Azure</span><span class="sxs-lookup"><span data-stu-id="79a35-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a35-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79a35-107">DESCRIPTION</span></span>
<span data-ttu-id="79a35-108">Il cmdlet **New-AzureRmRecoveryServicesAsrFabric** crea un tessuto di recupero del sito di Azure del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="79a35-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="79a35-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79a35-109">EXAMPLES</span></span>

### <span data-ttu-id="79a35-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79a35-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="79a35-111">Avvia la creazione del tessuto con il nome passato e restituisce il processo ASR usato per tenere traccia dell'operazione di creazione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="79a35-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="79a35-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="79a35-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="79a35-113">Avvia la creazione di tessuto Azure con il nome passato e restituisce il processo ASR usato per tenere traccia dell'operazione di creazione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="79a35-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="79a35-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79a35-114">PARAMETERS</span></span>

### <span data-ttu-id="79a35-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="79a35-115">-Azure</span></span>
<span data-ttu-id="79a35-116">Parametro switch indica la creazione di un tessuto Azure.</span><span class="sxs-lookup"><span data-stu-id="79a35-116">Switch parameter indicates creation of azure fabric.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a35-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79a35-117">-Confirm</span></span>
<span data-ttu-id="79a35-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a35-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a35-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a35-119">-DefaultProfile</span></span>
<span data-ttu-id="79a35-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79a35-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="79a35-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="79a35-121">-Location</span></span>
<span data-ttu-id="79a35-122">Specifica l'area di Azure corrispondente all'oggetto Fabric da creare.</span><span class="sxs-lookup"><span data-stu-id="79a35-122">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="79a35-123">L'oggetto tessuto di recupero sito di Azure rappresenta un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="79a35-123">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="79a35-124">Per le macchine virtuali replicate tra due aree di Azure, un tessuto principale rappresenta l'area di Azure primaria e il tessuto di recupero.</span><span class="sxs-lookup"><span data-stu-id="79a35-124">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a35-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="79a35-125">-Name</span></span>
<span data-ttu-id="79a35-126">Specifica il nome del tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="79a35-126">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a35-127">-Digitare</span><span class="sxs-lookup"><span data-stu-id="79a35-127">-Type</span></span>
<span data-ttu-id="79a35-128">Specifica il tipo di tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="79a35-128">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a35-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a35-129">-WhatIf</span></span>
<span data-ttu-id="79a35-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79a35-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79a35-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79a35-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a35-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a35-132">CommonParameters</span></span>
<span data-ttu-id="79a35-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a35-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a35-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a35-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a35-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79a35-135">INPUTS</span></span>

### <span data-ttu-id="79a35-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79a35-136">None</span></span>

## <span data-ttu-id="79a35-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79a35-137">OUTPUTS</span></span>

### <span data-ttu-id="79a35-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="79a35-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79a35-139">Note</span><span class="sxs-lookup"><span data-stu-id="79a35-139">NOTES</span></span>

## <span data-ttu-id="79a35-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79a35-140">RELATED LINKS</span></span>

[<span data-ttu-id="79a35-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="79a35-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="79a35-142">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="79a35-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)

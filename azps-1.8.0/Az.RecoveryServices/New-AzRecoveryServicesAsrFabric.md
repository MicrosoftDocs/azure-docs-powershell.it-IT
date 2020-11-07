---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8604d1a648590e0fc88a268e6bf2941bbf9344e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677630"
---
# <span data-ttu-id="473d0-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="473d0-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="473d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="473d0-102">SYNOPSIS</span></span>
<span data-ttu-id="473d0-103">Crea un tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="473d0-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="473d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="473d0-104">SYNTAX</span></span>

### <span data-ttu-id="473d0-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="473d0-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="473d0-106">Azure</span><span class="sxs-lookup"><span data-stu-id="473d0-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="473d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="473d0-107">DESCRIPTION</span></span>
<span data-ttu-id="473d0-108">Il cmdlet **New-AzRecoveryServicesAsrFabric** crea un tessuto di recupero del sito di Azure del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="473d0-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="473d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="473d0-109">EXAMPLES</span></span>

### <span data-ttu-id="473d0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="473d0-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="473d0-111">Avvia la creazione del tessuto con il nome passato e restituisce il processo ASR usato per tenere traccia dell'operazione di creazione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="473d0-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="473d0-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="473d0-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Az -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="473d0-113">Avvia la creazione di tessuto Azure con il nome passato e restituisce il processo ASR usato per tenere traccia dell'operazione di creazione del tessuto.</span><span class="sxs-lookup"><span data-stu-id="473d0-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="473d0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="473d0-114">PARAMETERS</span></span>

### <span data-ttu-id="473d0-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="473d0-115">-Azure</span></span>
<span data-ttu-id="473d0-116">{{Fill Azure Description}}</span><span class="sxs-lookup"><span data-stu-id="473d0-116">{{Fill Azure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473d0-117">-DefaultProfile</span></span>
<span data-ttu-id="473d0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="473d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="473d0-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="473d0-119">-Location</span></span>
<span data-ttu-id="473d0-120">Specifica l'area di Azure corrispondente all'oggetto Fabric da creare.</span><span class="sxs-lookup"><span data-stu-id="473d0-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="473d0-121">L'oggetto tessuto di recupero sito di Azure rappresenta un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="473d0-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="473d0-122">Per le macchine virtuali replicate tra due aree di Azure, un tessuto principale rappresenta l'area di Azure primaria e il tessuto di recupero.</span><span class="sxs-lookup"><span data-stu-id="473d0-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473d0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="473d0-123">-Name</span></span>
<span data-ttu-id="473d0-124">Specifica il nome del tessuto di recupero del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="473d0-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473d0-125">-Digitare</span><span class="sxs-lookup"><span data-stu-id="473d0-125">-Type</span></span>
<span data-ttu-id="473d0-126">Specifica il tipo di tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="473d0-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473d0-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="473d0-127">-Confirm</span></span>
<span data-ttu-id="473d0-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="473d0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="473d0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="473d0-129">-WhatIf</span></span>
<span data-ttu-id="473d0-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="473d0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="473d0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="473d0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="473d0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473d0-132">CommonParameters</span></span>
<span data-ttu-id="473d0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473d0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473d0-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473d0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473d0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="473d0-135">INPUTS</span></span>

### <span data-ttu-id="473d0-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="473d0-136">None</span></span>

## <span data-ttu-id="473d0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="473d0-137">OUTPUTS</span></span>

### <span data-ttu-id="473d0-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="473d0-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="473d0-139">Note</span><span class="sxs-lookup"><span data-stu-id="473d0-139">NOTES</span></span>

## <span data-ttu-id="473d0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="473d0-140">RELATED LINKS</span></span>

[<span data-ttu-id="473d0-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="473d0-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="473d0-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="473d0-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
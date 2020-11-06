---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: d17d01295d118c3927c127a367747cfde428ccfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508319"
---
# <span data-ttu-id="923c2-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="923c2-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="923c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="923c2-102">SYNOPSIS</span></span>
<span data-ttu-id="923c2-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="923c2-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="923c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="923c2-104">SYNTAX</span></span>

### <span data-ttu-id="923c2-105">GeneralizeResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="923c2-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="923c2-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="923c2-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="923c2-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="923c2-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="923c2-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="923c2-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="923c2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="923c2-109">DESCRIPTION</span></span>
<span data-ttu-id="923c2-110">Il cmdlet **set-AzureRmVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="923c2-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="923c2-111">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare Sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="923c2-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="923c2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="923c2-112">EXAMPLES</span></span>

### <span data-ttu-id="923c2-113">Esempio 1: contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="923c2-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="923c2-114">Questo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="923c2-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="923c2-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="923c2-115">PARAMETERS</span></span>

### <span data-ttu-id="923c2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="923c2-116">-AsJob</span></span>
<span data-ttu-id="923c2-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="923c2-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923c2-118">-DefaultProfile</span></span>
<span data-ttu-id="923c2-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="923c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="923c2-120">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="923c2-120">-Generalized</span></span>
<span data-ttu-id="923c2-121">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="923c2-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923c2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="923c2-122">-Id</span></span>
<span data-ttu-id="923c2-123">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="923c2-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="923c2-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="923c2-124">-Name</span></span>
<span data-ttu-id="923c2-125">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923c2-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="923c2-126">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="923c2-126">-Redeploy</span></span>
<span data-ttu-id="923c2-127">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale in un host Azure diverso per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="923c2-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="923c2-128">Se si ridistribuisce una macchina virtuale, viene riavviata, con la conseguenza della perdita di dati dell'unità effimera.</span><span class="sxs-lookup"><span data-stu-id="923c2-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923c2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923c2-129">-ResourceGroupName</span></span>
<span data-ttu-id="923c2-130">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="923c2-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="923c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923c2-131">CommonParameters</span></span>
<span data-ttu-id="923c2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923c2-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="923c2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923c2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="923c2-134">INPUTS</span></span>

### <span data-ttu-id="923c2-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="923c2-135">None</span></span>
<span data-ttu-id="923c2-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="923c2-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="923c2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="923c2-137">OUTPUTS</span></span>

### <span data-ttu-id="923c2-138">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="923c2-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="923c2-139">Note</span><span class="sxs-lookup"><span data-stu-id="923c2-139">NOTES</span></span>

## <span data-ttu-id="923c2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="923c2-140">RELATED LINKS</span></span>

[<span data-ttu-id="923c2-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="923c2-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


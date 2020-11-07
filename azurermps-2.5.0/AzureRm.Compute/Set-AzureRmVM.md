---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: 030e1dfc05354cded24ac76a379707edd0f07c34
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865930"
---
# <span data-ttu-id="e04e1-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e04e1-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="e04e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e04e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e04e1-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e04e1-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e04e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e04e1-104">SYNTAX</span></span>

### <span data-ttu-id="e04e1-105">GeneralizeResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e04e1-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e04e1-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e04e1-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e04e1-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e04e1-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e04e1-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e04e1-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e04e1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e04e1-109">DESCRIPTION</span></span>
<span data-ttu-id="e04e1-110">Il cmdlet **set-AzureRmVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e04e1-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="e04e1-111">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare Sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="e04e1-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="e04e1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e04e1-112">EXAMPLES</span></span>

### <span data-ttu-id="e04e1-113">Esempio 1: contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="e04e1-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="e04e1-114">Questo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e04e1-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="e04e1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e04e1-115">PARAMETERS</span></span>

### <span data-ttu-id="e04e1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e04e1-116">-AsJob</span></span>
<span data-ttu-id="e04e1-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e04e1-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e04e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04e1-118">-DefaultProfile</span></span>
<span data-ttu-id="e04e1-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e04e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e04e1-120">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="e04e1-120">-Generalized</span></span>
<span data-ttu-id="e04e1-121">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="e04e1-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="e04e1-122">-ID</span><span class="sxs-lookup"><span data-stu-id="e04e1-122">-Id</span></span>
<span data-ttu-id="e04e1-123">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e04e1-123">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e04e1-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e04e1-124">-Name</span></span>
<span data-ttu-id="e04e1-125">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e04e1-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e04e1-126">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="e04e1-126">-Redeploy</span></span>
<span data-ttu-id="e04e1-127">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale in un host Azure diverso per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="e04e1-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="e04e1-128">Se si ridistribuisce una macchina virtuale, viene riavviata, con la conseguenza della perdita di dati dell'unità effimera.</span><span class="sxs-lookup"><span data-stu-id="e04e1-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="e04e1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e04e1-129">-ResourceGroupName</span></span>
<span data-ttu-id="e04e1-130">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e04e1-130">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e04e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04e1-131">CommonParameters</span></span>
<span data-ttu-id="e04e1-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e04e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04e1-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04e1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04e1-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e04e1-134">INPUTS</span></span>

### <span data-ttu-id="e04e1-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e04e1-135">None</span></span>
<span data-ttu-id="e04e1-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e04e1-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e04e1-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e04e1-137">OUTPUTS</span></span>

### <span data-ttu-id="e04e1-138">Microsoft. Azure. Commands. Compute. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="e04e1-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="e04e1-139">Note</span><span class="sxs-lookup"><span data-stu-id="e04e1-139">NOTES</span></span>

## <span data-ttu-id="e04e1-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e04e1-140">RELATED LINKS</span></span>

[<span data-ttu-id="e04e1-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e04e1-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



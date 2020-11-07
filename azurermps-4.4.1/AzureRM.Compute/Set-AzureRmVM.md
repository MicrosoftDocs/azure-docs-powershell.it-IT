---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687540"
---
# <span data-ttu-id="71af8-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71af8-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="71af8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71af8-102">SYNOPSIS</span></span>
<span data-ttu-id="71af8-103">Contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="71af8-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71af8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71af8-104">SYNTAX</span></span>

### <span data-ttu-id="71af8-105">GeneralizeResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71af8-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71af8-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="71af8-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71af8-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="71af8-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71af8-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="71af8-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71af8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71af8-109">DESCRIPTION</span></span>
<span data-ttu-id="71af8-110">Il cmdlet **set-AzureRmVM** contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="71af8-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="71af8-111">Prima di eseguire questo cmdlet, accedere alla macchina virtuale e usare Sysprep per preparare il disco rigido.</span><span class="sxs-lookup"><span data-stu-id="71af8-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="71af8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71af8-112">EXAMPLES</span></span>

### <span data-ttu-id="71af8-113">Esempio 1: contrassegnare una macchina virtuale come generalizzata</span><span class="sxs-lookup"><span data-stu-id="71af8-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="71af8-114">Questo comando contrassegna la macchina virtuale denominata VirtualMachine07 come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="71af8-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="71af8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71af8-115">PARAMETERS</span></span>

### <span data-ttu-id="71af8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71af8-116">-DefaultProfile</span></span>
<span data-ttu-id="71af8-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71af8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71af8-118">-Generalizzato</span><span class="sxs-lookup"><span data-stu-id="71af8-118">-Generalized</span></span>
<span data-ttu-id="71af8-119">Indica che questo cmdlet contrassegna una macchina virtuale come generalizzata.</span><span class="sxs-lookup"><span data-stu-id="71af8-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71af8-120">-ID</span><span class="sxs-lookup"><span data-stu-id="71af8-120">-Id</span></span>
<span data-ttu-id="71af8-121">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="71af8-121">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71af8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="71af8-122">-Name</span></span>
<span data-ttu-id="71af8-123">Specifica il nome della macchina virtuale in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71af8-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71af8-124">-Ridistribuire</span><span class="sxs-lookup"><span data-stu-id="71af8-124">-Redeploy</span></span>
<span data-ttu-id="71af8-125">Indica che questo cmdlet ridistribuisce manualmente la macchina virtuale in un host Azure diverso per risolvere eventuali problemi.</span><span class="sxs-lookup"><span data-stu-id="71af8-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="71af8-126">Se si ridistribuisce una macchina virtuale, viene riavviata, con la conseguenza della perdita di dati dell'unità effimera.</span><span class="sxs-lookup"><span data-stu-id="71af8-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71af8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71af8-127">-ResourceGroupName</span></span>
<span data-ttu-id="71af8-128">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="71af8-128">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71af8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71af8-129">CommonParameters</span></span>
<span data-ttu-id="71af8-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71af8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71af8-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71af8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71af8-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71af8-132">INPUTS</span></span>

## <span data-ttu-id="71af8-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71af8-133">OUTPUTS</span></span>

## <span data-ttu-id="71af8-134">Note</span><span class="sxs-lookup"><span data-stu-id="71af8-134">NOTES</span></span>

## <span data-ttu-id="71af8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71af8-135">RELATED LINKS</span></span>

[<span data-ttu-id="71af8-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="71af8-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



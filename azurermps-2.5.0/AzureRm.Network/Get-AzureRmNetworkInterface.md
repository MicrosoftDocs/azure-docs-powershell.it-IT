---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 263293ea117f85caf32029ee0cfbf0dff2142cc3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867041"
---
# <span data-ttu-id="39153-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39153-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="39153-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39153-102">SYNOPSIS</span></span>
<span data-ttu-id="39153-103">Ottiene un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="39153-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39153-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39153-104">SYNTAX</span></span>

### <span data-ttu-id="39153-105">NoExpandStandAloneNic (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39153-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39153-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="39153-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39153-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="39153-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39153-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="39153-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39153-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39153-109">DESCRIPTION</span></span>
<span data-ttu-id="39153-110">Il cmdlet **Get-AzureRmNetworkInterface** ottiene un'interfaccia di rete Azure o un elenco di interfacce di rete Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39153-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="39153-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39153-111">EXAMPLES</span></span>

### <span data-ttu-id="39153-112">Esempio 1: ottenere tutte le interfacce di rete</span><span class="sxs-lookup"><span data-stu-id="39153-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="39153-113">Questo comando consente di ottenere tutte le interfacce di rete per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="39153-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="39153-114">Esempio 2: ottenere tutte le interfacce di rete con uno stato di provisioning specifico</span><span class="sxs-lookup"><span data-stu-id="39153-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="39153-115">Questo comando consente di ottenere tutte le interfacce di rete nel gruppo di risorse denominato ResourceGroup1 che ha uno stato di provisioning riuscito.</span><span class="sxs-lookup"><span data-stu-id="39153-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="39153-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39153-116">PARAMETERS</span></span>

### <span data-ttu-id="39153-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39153-117">-DefaultProfile</span></span>
<span data-ttu-id="39153-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39153-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39153-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="39153-119">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39153-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="39153-120">-Name</span></span>
<span data-ttu-id="39153-121">Specifica il nome dell'interfaccia di rete ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39153-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39153-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39153-122">-ResourceGroupName</span></span>
<span data-ttu-id="39153-123">Specifica il nome del gruppo di risorse da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="39153-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39153-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="39153-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="39153-125">Specifica l'indice della macchina virtuale del set di scale della macchina virtuale da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="39153-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39153-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="39153-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="39153-127">Specifica il nome del set di scale della macchina virtuale da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="39153-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandScaleSetNic
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetNic
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39153-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39153-128">CommonParameters</span></span>
<span data-ttu-id="39153-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39153-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39153-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39153-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39153-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39153-131">INPUTS</span></span>

## <span data-ttu-id="39153-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39153-132">OUTPUTS</span></span>

### <span data-ttu-id="39153-133">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39153-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="39153-134">Note</span><span class="sxs-lookup"><span data-stu-id="39153-134">NOTES</span></span>

## <span data-ttu-id="39153-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39153-135">RELATED LINKS</span></span>

[<span data-ttu-id="39153-136">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39153-136">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="39153-137">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39153-137">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="39153-138">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39153-138">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)



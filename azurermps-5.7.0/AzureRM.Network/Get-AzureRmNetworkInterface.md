---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: 00384e7765ec0ef47789a6ed1efa6c529bea10b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521896"
---
# <span data-ttu-id="dd231-101">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd231-101">Get-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="dd231-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd231-102">SYNOPSIS</span></span>
<span data-ttu-id="dd231-103">Ottiene un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="dd231-103">Gets a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd231-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd231-104">SYNTAX</span></span>

### <span data-ttu-id="dd231-105">NoExpandStandAloneNic (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dd231-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd231-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="dd231-106">ExpandStandAloneNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd231-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="dd231-107">NoExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd231-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="dd231-108">ExpandScaleSetNic</span></span>
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd231-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd231-109">DESCRIPTION</span></span>
<span data-ttu-id="dd231-110">Il cmdlet **Get-AzureRmNetworkInterface** ottiene un'interfaccia di rete Azure o un elenco di interfacce di rete Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd231-110">The **Get-AzureRmNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="dd231-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd231-111">EXAMPLES</span></span>

### <span data-ttu-id="dd231-112">Esempio 1: ottenere tutte le interfacce di rete</span><span class="sxs-lookup"><span data-stu-id="dd231-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzureRmNetworkInterface
```

<span data-ttu-id="dd231-113">Questo comando consente di ottenere tutte le interfacce di rete per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="dd231-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="dd231-114">Esempio 2: ottenere tutte le interfacce di rete con uno stato di provisioning specifico</span><span class="sxs-lookup"><span data-stu-id="dd231-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="dd231-115">Questo comando consente di ottenere tutte le interfacce di rete nel gruppo di risorse denominato ResourceGroup1 che ha uno stato di provisioning riuscito.</span><span class="sxs-lookup"><span data-stu-id="dd231-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="dd231-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd231-116">PARAMETERS</span></span>

### <span data-ttu-id="dd231-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd231-117">-DefaultProfile</span></span>
<span data-ttu-id="dd231-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd231-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd231-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="dd231-119">-ExpandResource</span></span>
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

### <span data-ttu-id="dd231-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd231-120">-Name</span></span>
<span data-ttu-id="dd231-121">Specifica il nome dell'interfaccia di rete ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd231-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dd231-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd231-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd231-123">Specifica il nome del gruppo di risorse da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="dd231-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="dd231-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="dd231-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="dd231-125">Specifica l'indice della macchina virtuale del set di scale della macchina virtuale da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="dd231-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="dd231-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dd231-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="dd231-127">Specifica il nome del set di scale della macchina virtuale da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="dd231-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="dd231-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd231-128">CommonParameters</span></span>
<span data-ttu-id="dd231-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd231-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd231-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd231-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd231-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd231-131">INPUTS</span></span>

### <span data-ttu-id="dd231-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dd231-132">None</span></span>
<span data-ttu-id="dd231-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="dd231-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd231-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd231-134">OUTPUTS</span></span>

### <span data-ttu-id="dd231-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd231-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="dd231-136">Note</span><span class="sxs-lookup"><span data-stu-id="dd231-136">NOTES</span></span>

## <span data-ttu-id="dd231-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd231-137">RELATED LINKS</span></span>

[<span data-ttu-id="dd231-138">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd231-138">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="dd231-139">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd231-139">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="dd231-140">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dd231-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)



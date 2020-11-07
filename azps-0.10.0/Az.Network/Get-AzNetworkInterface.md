---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: df769ff4a6e4eb47bc47b881ac8c06de1fdb9e4c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860758"
---
# <span data-ttu-id="f63de-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f63de-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="f63de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f63de-102">SYNOPSIS</span></span>
<span data-ttu-id="f63de-103">Ottiene un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f63de-103">Gets a network interface.</span></span>

## <span data-ttu-id="f63de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f63de-104">SYNTAX</span></span>

### <span data-ttu-id="f63de-105">NoExpandStandAloneNic (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f63de-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f63de-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="f63de-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f63de-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="f63de-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f63de-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="f63de-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f63de-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f63de-109">DESCRIPTION</span></span>
<span data-ttu-id="f63de-110">Il cmdlet **Get-AzNetworkInterface** ottiene un'interfaccia di rete Azure o un elenco di interfacce di rete Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f63de-110">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="f63de-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f63de-111">EXAMPLES</span></span>

### <span data-ttu-id="f63de-112">Esempio 1: ottenere tutte le interfacce di rete</span><span class="sxs-lookup"><span data-stu-id="f63de-112">Example 1: Get all network interfaces</span></span>
```
PS C:\>Get-AzNetworkInterface
```

<span data-ttu-id="f63de-113">Questo comando consente di ottenere tutte le interfacce di rete per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f63de-113">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="f63de-114">Esempio 2: ottenere tutte le interfacce di rete con uno stato di provisioning specifico</span><span class="sxs-lookup"><span data-stu-id="f63de-114">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\>Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

<span data-ttu-id="f63de-115">Questo comando consente di ottenere tutte le interfacce di rete nel gruppo di risorse denominato ResourceGroup1 che ha uno stato di provisioning riuscito.</span><span class="sxs-lookup"><span data-stu-id="f63de-115">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

## <span data-ttu-id="f63de-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f63de-116">PARAMETERS</span></span>

### <span data-ttu-id="f63de-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63de-117">-DefaultProfile</span></span>
<span data-ttu-id="f63de-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f63de-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f63de-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f63de-119">-ExpandResource</span></span>
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

### <span data-ttu-id="f63de-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f63de-120">-Name</span></span>
<span data-ttu-id="f63de-121">Specifica il nome dell'interfaccia di rete ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f63de-121">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f63de-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f63de-122">-ResourceGroupName</span></span>
<span data-ttu-id="f63de-123">Specifica il nome del gruppo di risorse da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="f63de-123">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="f63de-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="f63de-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="f63de-125">Specifica l'indice della macchina virtuale del set di scale della macchina virtuale da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="f63de-125">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="f63de-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f63de-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="f63de-127">Specifica il nome del set di scale della macchina virtuale da cui questo cmdlet ottiene le interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="f63de-127">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="f63de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63de-128">CommonParameters</span></span>
<span data-ttu-id="f63de-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f63de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63de-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f63de-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63de-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f63de-131">INPUTS</span></span>

## <span data-ttu-id="f63de-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f63de-132">OUTPUTS</span></span>

### <span data-ttu-id="f63de-133">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f63de-133">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f63de-134">Note</span><span class="sxs-lookup"><span data-stu-id="f63de-134">NOTES</span></span>

## <span data-ttu-id="f63de-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f63de-135">RELATED LINKS</span></span>

[<span data-ttu-id="f63de-136">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f63de-136">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="f63de-137">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f63de-137">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="f63de-138">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f63de-138">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)



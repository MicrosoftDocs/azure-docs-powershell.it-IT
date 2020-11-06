---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507584"
---
# <span data-ttu-id="0ac61-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="0ac61-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="0ac61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ac61-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac61-103">Crea un oggetto Tag IP per un'interfaccia di rete di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="0ac61-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ac61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ac61-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ac61-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ac61-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac61-106">Il cmdlet **New-AzureRmVmssIpTagConfig** crea un oggetto di configurazione di tag IP per un'interfaccia di rete di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0ac61-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0ac61-107">Specifica la configurazione di questo cmdlet come parametro *IPTag* del cmdlet New-AzureRmVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="0ac61-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="0ac61-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ac61-108">EXAMPLES</span></span>

### <span data-ttu-id="0ac61-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ac61-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="0ac61-110">Questo comando crea un oggetto local Tag IP con il tipo "FirstPartyUsage" e il tag "SQL" e quindi crea una configurazione IP con questo tag IP.</span><span class="sxs-lookup"><span data-stu-id="0ac61-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="0ac61-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ac61-111">PARAMETERS</span></span>

### <span data-ttu-id="0ac61-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac61-112">-DefaultProfile</span></span>
<span data-ttu-id="0ac61-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ac61-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ac61-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="0ac61-114">-IpTagType</span></span>
<span data-ttu-id="0ac61-115">Specifica un tipo di tag IP.</span><span class="sxs-lookup"><span data-stu-id="0ac61-115">Specifies an IP Tag Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac61-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ac61-116">-Tag</span></span>
<span data-ttu-id="0ac61-117">Specifica un valore di tag IP.</span><span class="sxs-lookup"><span data-stu-id="0ac61-117">Specifies an IP Tag Value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ac61-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ac61-118">-Confirm</span></span>
<span data-ttu-id="0ac61-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ac61-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac61-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac61-120">-WhatIf</span></span>
<span data-ttu-id="0ac61-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ac61-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ac61-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ac61-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac61-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac61-123">CommonParameters</span></span>
<span data-ttu-id="0ac61-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ac61-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac61-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac61-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac61-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ac61-126">INPUTS</span></span>

### <span data-ttu-id="0ac61-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0ac61-127">System.String</span></span>

## <span data-ttu-id="0ac61-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ac61-128">OUTPUTS</span></span>

### <span data-ttu-id="0ac61-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="0ac61-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="0ac61-130">Note</span><span class="sxs-lookup"><span data-stu-id="0ac61-130">NOTES</span></span>

## <span data-ttu-id="0ac61-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ac61-131">RELATED LINKS</span></span>

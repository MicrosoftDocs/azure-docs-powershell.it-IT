---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: 241b8938be77d9074000a116f82d8b2bcdffc5b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007070"
---
# <span data-ttu-id="83d4e-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="83d4e-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="83d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="83d4e-103">Crea un oggetto tag IP per un'interfaccia di rete di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="83d4e-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="83d4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83d4e-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83d4e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83d4e-105">DESCRIPTION</span></span>
<span data-ttu-id="83d4e-106">Il cmdlet **New-AzVmssIpTagConfig** crea un oggetto di configurazione del tag IP per un'interfaccia di rete di un set di scala di macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="83d4e-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="83d4e-107">Specificare la configurazione di questo cmdlet come *parametro IPTag* del cmdlet New-AzVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="83d4e-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="83d4e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83d4e-108">EXAMPLES</span></span>

### <span data-ttu-id="83d4e-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="83d4e-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="83d4e-110">Questo comando crea un oggetto locale di tag IP con tipo 'FirstPartyUsage' e tag 'Sql', quindi crea una configurazione IP con questo tag IP.</span><span class="sxs-lookup"><span data-stu-id="83d4e-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="83d4e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d4e-111">PARAMETERS</span></span>

### <span data-ttu-id="83d4e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d4e-112">-DefaultProfile</span></span>
<span data-ttu-id="83d4e-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83d4e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83d4e-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="83d4e-114">-IpTagType</span></span>
<span data-ttu-id="83d4e-115">Specifica un tipo di tag IP.</span><span class="sxs-lookup"><span data-stu-id="83d4e-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="83d4e-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="83d4e-116">-Tag</span></span>
<span data-ttu-id="83d4e-117">Specifica un valore di tag IP.</span><span class="sxs-lookup"><span data-stu-id="83d4e-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="83d4e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83d4e-118">-Confirm</span></span>
<span data-ttu-id="83d4e-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83d4e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83d4e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83d4e-120">-WhatIf</span></span>
<span data-ttu-id="83d4e-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83d4e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83d4e-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83d4e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83d4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d4e-123">CommonParameters</span></span>
<span data-ttu-id="83d4e-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d4e-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83d4e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d4e-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="83d4e-126">INPUTS</span></span>

### <span data-ttu-id="83d4e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="83d4e-127">System.String</span></span>

## <span data-ttu-id="83d4e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83d4e-128">OUTPUTS</span></span>

### <span data-ttu-id="83d4e-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="83d4e-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="83d4e-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="83d4e-130">NOTES</span></span>

## <span data-ttu-id="83d4e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83d4e-131">RELATED LINKS</span></span>

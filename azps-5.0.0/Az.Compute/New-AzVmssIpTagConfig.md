---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300769"
---
# <span data-ttu-id="9dc8c-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="9dc8c-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="9dc8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9dc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc8c-103">Crea un oggetto Tag IP per un'interfaccia di rete di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="9dc8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9dc8c-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc8c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9dc8c-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc8c-106">Il cmdlet **New-AzVmssIpTagConfig** crea un oggetto di configurazione di tag IP per un'interfaccia di rete di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9dc8c-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9dc8c-107">Specifica la configurazione di questo cmdlet come parametro *IPTag* del cmdlet New-AzVmssIpConfig.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="9dc8c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9dc8c-108">EXAMPLES</span></span>

### <span data-ttu-id="9dc8c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9dc8c-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="9dc8c-110">Questo comando crea un oggetto local Tag IP con il tipo "FirstPartyUsage" e il tag "SQL" e quindi crea una configurazione IP con questo tag IP.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="9dc8c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9dc8c-111">PARAMETERS</span></span>

### <span data-ttu-id="9dc8c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc8c-112">-DefaultProfile</span></span>
<span data-ttu-id="9dc8c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dc8c-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="9dc8c-114">-IpTagType</span></span>
<span data-ttu-id="9dc8c-115">Specifica un tipo di tag IP.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="9dc8c-116">-Tag</span><span class="sxs-lookup"><span data-stu-id="9dc8c-116">-Tag</span></span>
<span data-ttu-id="9dc8c-117">Specifica un valore di tag IP.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="9dc8c-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9dc8c-118">-Confirm</span></span>
<span data-ttu-id="9dc8c-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc8c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc8c-120">-WhatIf</span></span>
<span data-ttu-id="9dc8c-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dc8c-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc8c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc8c-123">CommonParameters</span></span>
<span data-ttu-id="9dc8c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc8c-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9dc8c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc8c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9dc8c-126">INPUTS</span></span>

### <span data-ttu-id="9dc8c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9dc8c-127">System.String</span></span>

## <span data-ttu-id="9dc8c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9dc8c-128">OUTPUTS</span></span>

### <span data-ttu-id="9dc8c-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="9dc8c-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="9dc8c-130">Note</span><span class="sxs-lookup"><span data-stu-id="9dc8c-130">NOTES</span></span>

## <span data-ttu-id="9dc8c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9dc8c-131">RELATED LINKS</span></span>

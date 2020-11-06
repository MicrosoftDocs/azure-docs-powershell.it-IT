---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 6931f6d80d3e279259b599b782a505b2a21dd074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521761"
---
# <span data-ttu-id="a40fd-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a40fd-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="a40fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a40fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a40fd-103">Converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="a40fd-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a40fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a40fd-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a40fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40fd-105">DESCRIPTION</span></span>
<span data-ttu-id="a40fd-106">Il cmdlet **ConvertTo-AzureRmVMManagedDisk** converte una macchina virtuale con dischi basati su BLOB in una macchina virtuale con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="a40fd-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="a40fd-107">Prima di richiamare l'operazione, la macchina virtuale deve essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="a40fd-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="a40fd-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a40fd-108">EXAMPLES</span></span>

### <span data-ttu-id="a40fd-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a40fd-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="a40fd-110">Questo comando converte i dischi basati su BLOB della macchina virtuale denominata "VM01" nel gruppo di risorse "ResourceGroup01" in dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="a40fd-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="a40fd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a40fd-111">PARAMETERS</span></span>

### <span data-ttu-id="a40fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40fd-112">-DefaultProfile</span></span>
<span data-ttu-id="a40fd-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a40fd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a40fd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40fd-114">-ResourceGroupName</span></span>
<span data-ttu-id="a40fd-115">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a40fd-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a40fd-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="a40fd-116">-VMName</span></span>
<span data-ttu-id="a40fd-117">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a40fd-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40fd-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a40fd-118">-Confirm</span></span>
<span data-ttu-id="a40fd-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a40fd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a40fd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a40fd-120">-WhatIf</span></span>
<span data-ttu-id="a40fd-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a40fd-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a40fd-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a40fd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a40fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40fd-123">CommonParameters</span></span>
<span data-ttu-id="a40fd-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40fd-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40fd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40fd-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a40fd-126">INPUTS</span></span>

### <span data-ttu-id="a40fd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a40fd-127">System.String</span></span>

## <span data-ttu-id="a40fd-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a40fd-128">OUTPUTS</span></span>

### <span data-ttu-id="a40fd-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="a40fd-129">System.Object</span></span>

## <span data-ttu-id="a40fd-130">Note</span><span class="sxs-lookup"><span data-stu-id="a40fd-130">NOTES</span></span>

## <span data-ttu-id="a40fd-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a40fd-131">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 1c2b58d58303dba38f907e9019f45502218c345a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675262"
---
# <span data-ttu-id="e1d34-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="e1d34-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="e1d34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1d34-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d34-103">Rimuove il backup da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1d34-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="e1d34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1d34-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1d34-105">DESCRIPTION</span></span>

## <span data-ttu-id="e1d34-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1d34-106">EXAMPLES</span></span>

### <span data-ttu-id="e1d34-107">1:</span><span class="sxs-lookup"><span data-stu-id="e1d34-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e1d34-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1d34-108">PARAMETERS</span></span>

### <span data-ttu-id="e1d34-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d34-109">-DefaultProfile</span></span>
<span data-ttu-id="e1d34-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d34-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d34-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d34-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e1d34-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1d34-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d34-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="e1d34-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d34-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d34-114">CommonParameters</span></span>
<span data-ttu-id="e1d34-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d34-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d34-116">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1d34-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d34-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1d34-117">INPUTS</span></span>

### <span data-ttu-id="e1d34-118">System. String</span><span class="sxs-lookup"><span data-stu-id="e1d34-118">System.String</span></span>

## <span data-ttu-id="e1d34-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1d34-119">OUTPUTS</span></span>

### <span data-ttu-id="e1d34-120">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e1d34-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e1d34-121">Note</span><span class="sxs-lookup"><span data-stu-id="e1d34-121">NOTES</span></span>

## <span data-ttu-id="e1d34-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1d34-122">RELATED LINKS</span></span>

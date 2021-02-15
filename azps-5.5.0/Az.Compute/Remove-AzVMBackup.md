---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177567"
---
# <span data-ttu-id="9c8a5-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="9c8a5-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="9c8a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8a5-103">Rimuove il backup da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="9c8a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c8a5-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c8a5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c8a5-105">DESCRIPTION</span></span>

## <span data-ttu-id="9c8a5-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c8a5-106">EXAMPLES</span></span>

### <span data-ttu-id="9c8a5-107">1:</span><span class="sxs-lookup"><span data-stu-id="9c8a5-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9c8a5-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c8a5-108">PARAMETERS</span></span>

### <span data-ttu-id="9c8a5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8a5-109">-DefaultProfile</span></span>
<span data-ttu-id="9c8a5-110">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c8a5-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c8a5-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9c8a5-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c8a5-112">-Tag</span></span>
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

### <span data-ttu-id="9c8a5-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="9c8a5-113">-VMName</span></span>
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

### <span data-ttu-id="9c8a5-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8a5-114">CommonParameters</span></span>
<span data-ttu-id="9c8a5-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8a5-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c8a5-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8a5-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c8a5-117">INPUTS</span></span>

### <span data-ttu-id="9c8a5-118">System.String</span><span class="sxs-lookup"><span data-stu-id="9c8a5-118">System.String</span></span>

## <span data-ttu-id="9c8a5-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c8a5-119">OUTPUTS</span></span>

### <span data-ttu-id="9c8a5-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c8a5-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9c8a5-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c8a5-121">NOTES</span></span>

## <span data-ttu-id="9c8a5-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c8a5-122">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 7be9116814af3f11e6bd61668b77df133676ab1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013694"
---
# <span data-ttu-id="f4083-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="f4083-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="f4083-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4083-102">SYNOPSIS</span></span>
<span data-ttu-id="f4083-103">Imposta le proprietà dell'estensione di backup in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f4083-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="f4083-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4083-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4083-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4083-105">DESCRIPTION</span></span>

## <span data-ttu-id="f4083-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4083-106">EXAMPLES</span></span>

### <span data-ttu-id="f4083-107">1:</span><span class="sxs-lookup"><span data-stu-id="f4083-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f4083-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4083-108">PARAMETERS</span></span>

### <span data-ttu-id="f4083-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4083-109">-DefaultProfile</span></span>
<span data-ttu-id="f4083-110">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4083-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4083-111">-Name</span><span class="sxs-lookup"><span data-stu-id="f4083-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4083-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4083-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f4083-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4083-113">-Tag</span></span>
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

### <span data-ttu-id="f4083-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="f4083-114">-VMName</span></span>
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

### <span data-ttu-id="f4083-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4083-115">CommonParameters</span></span>
<span data-ttu-id="f4083-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4083-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4083-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4083-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4083-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4083-118">INPUTS</span></span>

### <span data-ttu-id="f4083-119">System.String</span><span class="sxs-lookup"><span data-stu-id="f4083-119">System.String</span></span>

## <span data-ttu-id="f4083-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4083-120">OUTPUTS</span></span>

### <span data-ttu-id="f4083-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f4083-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f4083-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4083-122">NOTES</span></span>

## <span data-ttu-id="f4083-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4083-123">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340387"
---
# <span data-ttu-id="683a6-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="683a6-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="683a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="683a6-102">SYNOPSIS</span></span>
<span data-ttu-id="683a6-103">Imposta le proprietà delle estensioni di backup in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="683a6-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="683a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="683a6-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="683a6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="683a6-105">DESCRIPTION</span></span>

## <span data-ttu-id="683a6-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="683a6-106">EXAMPLES</span></span>

### <span data-ttu-id="683a6-107">1:</span><span class="sxs-lookup"><span data-stu-id="683a6-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="683a6-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="683a6-108">PARAMETERS</span></span>

### <span data-ttu-id="683a6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683a6-109">-DefaultProfile</span></span>
<span data-ttu-id="683a6-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="683a6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="683a6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="683a6-111">-Name</span></span>
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

### <span data-ttu-id="683a6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683a6-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="683a6-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="683a6-113">-Tag</span></span>
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

### <span data-ttu-id="683a6-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="683a6-114">-VMName</span></span>
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

### <span data-ttu-id="683a6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683a6-115">CommonParameters</span></span>
<span data-ttu-id="683a6-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683a6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683a6-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="683a6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683a6-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="683a6-118">INPUTS</span></span>

### <span data-ttu-id="683a6-119">System. String</span><span class="sxs-lookup"><span data-stu-id="683a6-119">System.String</span></span>

## <span data-ttu-id="683a6-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="683a6-120">OUTPUTS</span></span>

### <span data-ttu-id="683a6-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="683a6-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="683a6-122">Note</span><span class="sxs-lookup"><span data-stu-id="683a6-122">NOTES</span></span>

## <span data-ttu-id="683a6-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="683a6-123">RELATED LINKS</span></span>

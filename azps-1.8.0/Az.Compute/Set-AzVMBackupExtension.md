---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 1f4844ae499f68031af89e801023c849577794f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836664"
---
# <span data-ttu-id="b7be0-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="b7be0-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="b7be0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7be0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7be0-103">Imposta le proprietà delle estensioni di backup in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7be0-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="b7be0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7be0-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7be0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7be0-105">DESCRIPTION</span></span>

## <span data-ttu-id="b7be0-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7be0-106">EXAMPLES</span></span>

### <span data-ttu-id="b7be0-107">1:</span><span class="sxs-lookup"><span data-stu-id="b7be0-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b7be0-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7be0-108">PARAMETERS</span></span>

### <span data-ttu-id="b7be0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7be0-109">-DefaultProfile</span></span>
<span data-ttu-id="b7be0-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7be0-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7be0-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7be0-111">-Name</span></span>
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

### <span data-ttu-id="b7be0-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7be0-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b7be0-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7be0-113">-Tag</span></span>
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

### <span data-ttu-id="b7be0-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="b7be0-114">-VMName</span></span>
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

### <span data-ttu-id="b7be0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7be0-115">CommonParameters</span></span>
<span data-ttu-id="b7be0-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7be0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7be0-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7be0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7be0-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7be0-118">INPUTS</span></span>

### <span data-ttu-id="b7be0-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b7be0-119">System.String</span></span>

## <span data-ttu-id="b7be0-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7be0-120">OUTPUTS</span></span>

### <span data-ttu-id="b7be0-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b7be0-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b7be0-122">Note</span><span class="sxs-lookup"><span data-stu-id="b7be0-122">NOTES</span></span>

## <span data-ttu-id="b7be0-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7be0-123">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: dfcbc8c9b39faae2212bb26098bcfe0f2a966a3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675188"
---
# <span data-ttu-id="0771d-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="0771d-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="0771d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0771d-102">SYNOPSIS</span></span>
<span data-ttu-id="0771d-103">Imposta le proprietà delle estensioni di backup in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0771d-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="0771d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0771d-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0771d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0771d-105">DESCRIPTION</span></span>

## <span data-ttu-id="0771d-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0771d-106">EXAMPLES</span></span>

### <span data-ttu-id="0771d-107">1:</span><span class="sxs-lookup"><span data-stu-id="0771d-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0771d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0771d-108">PARAMETERS</span></span>

### <span data-ttu-id="0771d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0771d-109">-DefaultProfile</span></span>
<span data-ttu-id="0771d-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0771d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0771d-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="0771d-111">-Name</span></span>
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

### <span data-ttu-id="0771d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0771d-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0771d-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="0771d-113">-Tag</span></span>
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

### <span data-ttu-id="0771d-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="0771d-114">-VMName</span></span>
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

### <span data-ttu-id="0771d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0771d-115">CommonParameters</span></span>
<span data-ttu-id="0771d-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0771d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0771d-117">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0771d-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0771d-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0771d-118">INPUTS</span></span>

### <span data-ttu-id="0771d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0771d-119">System.String</span></span>

## <span data-ttu-id="0771d-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0771d-120">OUTPUTS</span></span>

### <span data-ttu-id="0771d-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0771d-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0771d-122">Note</span><span class="sxs-lookup"><span data-stu-id="0771d-122">NOTES</span></span>

## <span data-ttu-id="0771d-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0771d-123">RELATED LINKS</span></span>

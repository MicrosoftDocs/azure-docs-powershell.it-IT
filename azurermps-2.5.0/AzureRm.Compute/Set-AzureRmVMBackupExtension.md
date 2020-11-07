---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866528"
---
# <span data-ttu-id="fbbb6-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="fbbb6-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="fbbb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbbb6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb6-103">Imposta le proprietà delle estensioni di backup in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbbb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbbb6-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbbb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbbb6-105">DESCRIPTION</span></span>

## <span data-ttu-id="fbbb6-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbbb6-106">EXAMPLES</span></span>

### <span data-ttu-id="fbbb6-107">1:</span><span class="sxs-lookup"><span data-stu-id="fbbb6-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fbbb6-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbbb6-108">PARAMETERS</span></span>

### <span data-ttu-id="fbbb6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbb6-109">-DefaultProfile</span></span>
<span data-ttu-id="fbbb6-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbbb6-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbb6-112">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbbb6-113">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="fbbb6-114">-VMName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb6-115">CommonParameters</span></span>
<span data-ttu-id="fbbb6-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb6-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbb6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb6-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbbb6-118">INPUTS</span></span>

### <span data-ttu-id="fbbb6-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fbbb6-119">None</span></span>
<span data-ttu-id="fbbb6-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fbbb6-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbbb6-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbbb6-121">OUTPUTS</span></span>

### <span data-ttu-id="fbbb6-122">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fbbb6-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fbbb6-123">Note</span><span class="sxs-lookup"><span data-stu-id="fbbb6-123">NOTES</span></span>

## <span data-ttu-id="fbbb6-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbbb6-124">RELATED LINKS</span></span>


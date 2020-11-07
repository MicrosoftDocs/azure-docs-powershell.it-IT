---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866712"
---
# <span data-ttu-id="d1aa2-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="d1aa2-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="d1aa2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="d1aa2-103">Rimuove il backup da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1aa2-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1aa2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1aa2-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1aa2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1aa2-105">DESCRIPTION</span></span>

## <span data-ttu-id="d1aa2-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1aa2-106">EXAMPLES</span></span>

### <span data-ttu-id="d1aa2-107">1:</span><span class="sxs-lookup"><span data-stu-id="d1aa2-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d1aa2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1aa2-108">PARAMETERS</span></span>

### <span data-ttu-id="d1aa2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1aa2-109">-DefaultProfile</span></span>
<span data-ttu-id="d1aa2-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1aa2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1aa2-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1aa2-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d1aa2-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1aa2-112">-Tag</span></span>
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

### <span data-ttu-id="d1aa2-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="d1aa2-113">-VMName</span></span>
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

### <span data-ttu-id="d1aa2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1aa2-114">CommonParameters</span></span>
<span data-ttu-id="d1aa2-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1aa2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1aa2-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1aa2-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1aa2-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1aa2-117">INPUTS</span></span>

### <span data-ttu-id="d1aa2-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d1aa2-118">None</span></span>
<span data-ttu-id="d1aa2-119">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d1aa2-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1aa2-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1aa2-120">OUTPUTS</span></span>

### <span data-ttu-id="d1aa2-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d1aa2-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d1aa2-122">Note</span><span class="sxs-lookup"><span data-stu-id="d1aa2-122">NOTES</span></span>

## <span data-ttu-id="d1aa2-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1aa2-123">RELATED LINKS</span></span>


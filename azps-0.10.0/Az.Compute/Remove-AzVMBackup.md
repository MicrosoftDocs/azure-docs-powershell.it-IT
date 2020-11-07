---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863550"
---
# <span data-ttu-id="b01a1-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="b01a1-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="b01a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b01a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b01a1-103">Rimuove il backup da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b01a1-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="b01a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b01a1-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b01a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b01a1-105">DESCRIPTION</span></span>

## <span data-ttu-id="b01a1-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b01a1-106">EXAMPLES</span></span>

### <span data-ttu-id="b01a1-107">1:</span><span class="sxs-lookup"><span data-stu-id="b01a1-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b01a1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b01a1-108">PARAMETERS</span></span>

### <span data-ttu-id="b01a1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01a1-109">-DefaultProfile</span></span>
<span data-ttu-id="b01a1-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b01a1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01a1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b01a1-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b01a1-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="b01a1-112">-Tag</span></span>
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

### <span data-ttu-id="b01a1-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="b01a1-113">-VMName</span></span>
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

### <span data-ttu-id="b01a1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01a1-114">CommonParameters</span></span>
<span data-ttu-id="b01a1-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b01a1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01a1-116">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b01a1-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01a1-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b01a1-117">INPUTS</span></span>

### <span data-ttu-id="b01a1-118">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b01a1-118">None</span></span>
<span data-ttu-id="b01a1-119">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b01a1-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b01a1-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b01a1-120">OUTPUTS</span></span>

### <span data-ttu-id="b01a1-121">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b01a1-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b01a1-122">Note</span><span class="sxs-lookup"><span data-stu-id="b01a1-122">NOTES</span></span>

## <span data-ttu-id="b01a1-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b01a1-123">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863401"
---
# <span data-ttu-id="af325-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="af325-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="af325-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af325-102">SYNOPSIS</span></span>
<span data-ttu-id="af325-103">Imposta le proprietà delle estensioni di backup in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="af325-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="af325-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af325-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af325-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af325-105">DESCRIPTION</span></span>

## <span data-ttu-id="af325-106">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af325-106">EXAMPLES</span></span>

### <span data-ttu-id="af325-107">1:</span><span class="sxs-lookup"><span data-stu-id="af325-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="af325-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af325-108">PARAMETERS</span></span>

### <span data-ttu-id="af325-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af325-109">-DefaultProfile</span></span>
<span data-ttu-id="af325-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af325-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af325-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="af325-111">-Name</span></span>
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

### <span data-ttu-id="af325-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af325-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="af325-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="af325-113">-Tag</span></span>
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

### <span data-ttu-id="af325-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="af325-114">-VMName</span></span>
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

### <span data-ttu-id="af325-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af325-115">CommonParameters</span></span>
<span data-ttu-id="af325-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af325-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af325-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af325-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af325-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af325-118">INPUTS</span></span>

### <span data-ttu-id="af325-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="af325-119">None</span></span>
<span data-ttu-id="af325-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="af325-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af325-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af325-121">OUTPUTS</span></span>

### <span data-ttu-id="af325-122">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="af325-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="af325-123">Note</span><span class="sxs-lookup"><span data-stu-id="af325-123">NOTES</span></span>

## <span data-ttu-id="af325-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af325-124">RELATED LINKS</span></span>


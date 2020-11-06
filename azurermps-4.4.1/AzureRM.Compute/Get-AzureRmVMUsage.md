---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: af360334ab546685deadad45c2ea3f8954c226f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519603"
---
# <span data-ttu-id="1f048-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="1f048-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="1f048-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f048-102">SYNOPSIS</span></span>
<span data-ttu-id="1f048-103">Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="1f048-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f048-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f048-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f048-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f048-105">DESCRIPTION</span></span>
<span data-ttu-id="1f048-106">Il cmdlet **Get-AzureRmVMUsage** Ottiene l'utilizzo del numero di core della macchina virtuale per una posizione.</span><span class="sxs-lookup"><span data-stu-id="1f048-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1f048-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f048-107">EXAMPLES</span></span>

### <span data-ttu-id="1f048-108">Esempio 1: ottenere l'utilizzo del numero di base per una posizione</span><span class="sxs-lookup"><span data-stu-id="1f048-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="1f048-109">Questo comando ottiene l'utilizzo del numero di core della macchina virtuale per l'ubicazione centrale degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="1f048-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="1f048-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f048-110">PARAMETERS</span></span>

### <span data-ttu-id="1f048-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f048-111">-DefaultProfile</span></span>
<span data-ttu-id="1f048-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f048-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f048-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1f048-113">-Location</span></span>
<span data-ttu-id="1f048-114">Specifica la posizione per cui questo cmdlet ottiene l'utilizzo del numero di core della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1f048-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="1f048-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f048-115">CommonParameters</span></span>
<span data-ttu-id="1f048-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f048-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f048-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f048-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f048-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f048-118">INPUTS</span></span>

## <span data-ttu-id="1f048-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f048-119">OUTPUTS</span></span>

## <span data-ttu-id="1f048-120">Note</span><span class="sxs-lookup"><span data-stu-id="1f048-120">NOTES</span></span>

## <span data-ttu-id="1f048-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f048-121">RELATED LINKS</span></span>

[<span data-ttu-id="1f048-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1f048-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



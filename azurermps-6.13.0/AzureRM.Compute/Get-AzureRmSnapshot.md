---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 14b1c1179e9fee15f398c4518e446cf47396e660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511867"
---
# <span data-ttu-id="35555-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="35555-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="35555-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35555-102">SYNOPSIS</span></span>
<span data-ttu-id="35555-103">Ottiene le proprietà di uno snapshot</span><span class="sxs-lookup"><span data-stu-id="35555-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35555-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35555-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35555-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35555-105">DESCRIPTION</span></span>
<span data-ttu-id="35555-106">Il cmdlet **Get-AzureRmSnapshot** ottiene le proprietà di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="35555-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="35555-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35555-107">EXAMPLES</span></span>

### <span data-ttu-id="35555-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35555-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="35555-109">Questo comando consente di ottenere le proprietà di tutti gli snapshot dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="35555-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="35555-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="35555-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="35555-111">Questo comando consente di ottenere le proprietà di tutti gli snapshot nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="35555-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="35555-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="35555-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="35555-113">Questo comando consente di ottenere le proprietà dello snapshot denominato "SnapshotName1" nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="35555-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="35555-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35555-114">PARAMETERS</span></span>

### <span data-ttu-id="35555-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35555-115">-DefaultProfile</span></span>
<span data-ttu-id="35555-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35555-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35555-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35555-117">-ResourceGroupName</span></span>
<span data-ttu-id="35555-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35555-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35555-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="35555-119">-SnapshotName</span></span>
<span data-ttu-id="35555-120">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="35555-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35555-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35555-121">CommonParameters</span></span>
<span data-ttu-id="35555-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35555-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35555-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35555-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35555-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35555-124">INPUTS</span></span>

### <span data-ttu-id="35555-125">System. String</span><span class="sxs-lookup"><span data-stu-id="35555-125">System.String</span></span>

## <span data-ttu-id="35555-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35555-126">OUTPUTS</span></span>

### <span data-ttu-id="35555-127">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="35555-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="35555-128">Note</span><span class="sxs-lookup"><span data-stu-id="35555-128">NOTES</span></span>

## <span data-ttu-id="35555-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35555-129">RELATED LINKS</span></span>

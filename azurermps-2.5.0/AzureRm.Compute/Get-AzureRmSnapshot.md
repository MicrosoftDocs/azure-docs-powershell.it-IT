---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866140"
---
# <span data-ttu-id="67cd9-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="67cd9-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="67cd9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="67cd9-103">Ottiene le proprietà di uno snapshot</span><span class="sxs-lookup"><span data-stu-id="67cd9-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67cd9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67cd9-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67cd9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="67cd9-106">Il cmdlet **Get-AzureRmSnapshot** ottiene le proprietà di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="67cd9-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="67cd9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67cd9-107">EXAMPLES</span></span>

### <span data-ttu-id="67cd9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="67cd9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="67cd9-109">Questo comando consente di ottenere le proprietà di tutti gli snapshot dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="67cd9-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="67cd9-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="67cd9-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="67cd9-111">Questo comando consente di ottenere le proprietà di tutti gli snapshot nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="67cd9-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="67cd9-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="67cd9-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="67cd9-113">Questo comando consente di ottenere le proprietà dello snapshot denominato "SnapshotName1" nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="67cd9-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="67cd9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67cd9-114">PARAMETERS</span></span>

### <span data-ttu-id="67cd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67cd9-115">-DefaultProfile</span></span>
<span data-ttu-id="67cd9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67cd9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67cd9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67cd9-117">-ResourceGroupName</span></span>
<span data-ttu-id="67cd9-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67cd9-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67cd9-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="67cd9-119">-SnapshotName</span></span>
<span data-ttu-id="67cd9-120">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="67cd9-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67cd9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67cd9-121">CommonParameters</span></span>
<span data-ttu-id="67cd9-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67cd9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67cd9-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67cd9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67cd9-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67cd9-124">INPUTS</span></span>

### <span data-ttu-id="67cd9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="67cd9-125">System.String</span></span>

## <span data-ttu-id="67cd9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67cd9-126">OUTPUTS</span></span>

### <span data-ttu-id="67cd9-127">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="67cd9-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="67cd9-128">Note</span><span class="sxs-lookup"><span data-stu-id="67cd9-128">NOTES</span></span>

## <span data-ttu-id="67cd9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67cd9-129">RELATED LINKS</span></span>


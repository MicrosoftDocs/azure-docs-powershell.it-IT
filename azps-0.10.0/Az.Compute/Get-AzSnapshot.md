---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863813"
---
# <span data-ttu-id="f3280-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="f3280-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="f3280-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3280-102">SYNOPSIS</span></span>
<span data-ttu-id="f3280-103">Ottiene le proprietà di uno snapshot</span><span class="sxs-lookup"><span data-stu-id="f3280-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="f3280-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3280-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3280-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3280-105">DESCRIPTION</span></span>
<span data-ttu-id="f3280-106">Il cmdlet **Get-AzSnapshot** ottiene le proprietà di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="f3280-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="f3280-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3280-107">EXAMPLES</span></span>

### <span data-ttu-id="f3280-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3280-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="f3280-109">Questo comando consente di ottenere le proprietà di tutti gli snapshot dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f3280-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="f3280-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f3280-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="f3280-111">Questo comando consente di ottenere le proprietà di tutti gli snapshot nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="f3280-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="f3280-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f3280-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="f3280-113">Questo comando consente di ottenere le proprietà dello snapshot denominato "SnapshotName1" nel gruppo di risorse denominato "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="f3280-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="f3280-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3280-114">PARAMETERS</span></span>

### <span data-ttu-id="f3280-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3280-115">-DefaultProfile</span></span>
<span data-ttu-id="f3280-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3280-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3280-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3280-117">-ResourceGroupName</span></span>
<span data-ttu-id="f3280-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3280-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f3280-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="f3280-119">-SnapshotName</span></span>
<span data-ttu-id="f3280-120">Specifica il nome di uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="f3280-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="f3280-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3280-121">CommonParameters</span></span>
<span data-ttu-id="f3280-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3280-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3280-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3280-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3280-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3280-124">INPUTS</span></span>

### <span data-ttu-id="f3280-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f3280-125">System.String</span></span>

## <span data-ttu-id="f3280-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3280-126">OUTPUTS</span></span>

### <span data-ttu-id="f3280-127">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="f3280-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="f3280-128">Note</span><span class="sxs-lookup"><span data-stu-id="f3280-128">NOTES</span></span>

## <span data-ttu-id="f3280-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3280-129">RELATED LINKS</span></span>


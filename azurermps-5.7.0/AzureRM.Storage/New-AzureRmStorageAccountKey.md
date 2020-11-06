---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519342"
---
# <span data-ttu-id="d0f13-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0f13-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="d0f13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0f13-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f13-103">Rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f13-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0f13-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="d0f13-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0f13-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f13-106">Il cmdlet **New-AzureRmStorageAccountKey** rigenera una chiave di archiviazione per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f13-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="d0f13-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0f13-107">EXAMPLES</span></span>

### <span data-ttu-id="d0f13-108">Esempio 1: rigenerare una chiave di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d0f13-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="d0f13-109">Questo comando rigenera una chiave di archiviazione per l'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="d0f13-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="d0f13-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0f13-110">PARAMETERS</span></span>

### <span data-ttu-id="d0f13-111">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="d0f13-111">-KeyName</span></span>
<span data-ttu-id="d0f13-112">Specifica il tasto da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="d0f13-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="d0f13-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0f13-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0f13-114">Key1</span><span class="sxs-lookup"><span data-stu-id="d0f13-114">key1</span></span>
- <span data-ttu-id="d0f13-115">Key2</span><span class="sxs-lookup"><span data-stu-id="d0f13-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f13-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0f13-116">-Name</span></span>
<span data-ttu-id="d0f13-117">Specifica il nome dell'account di archiviazione per cui rigenerare una chiave di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0f13-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f13-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f13-118">-ResourceGroupName</span></span>
<span data-ttu-id="d0f13-119">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0f13-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="d0f13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f13-120">CommonParameters</span></span>
<span data-ttu-id="d0f13-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f13-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f13-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f13-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0f13-123">INPUTS</span></span>

### <span data-ttu-id="d0f13-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d0f13-124">None</span></span>
<span data-ttu-id="d0f13-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d0f13-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0f13-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0f13-126">OUTPUTS</span></span>

## <span data-ttu-id="d0f13-127">Note</span><span class="sxs-lookup"><span data-stu-id="d0f13-127">NOTES</span></span>

## <span data-ttu-id="d0f13-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0f13-128">RELATED LINKS</span></span>

[<span data-ttu-id="d0f13-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0f13-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)

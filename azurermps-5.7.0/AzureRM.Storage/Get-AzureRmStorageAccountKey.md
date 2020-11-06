---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509559"
---
# <span data-ttu-id="607fd-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="607fd-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="607fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="607fd-102">SYNOPSIS</span></span>
<span data-ttu-id="607fd-103">Ottiene i tasti di scelta per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="607fd-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="607fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="607fd-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="607fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="607fd-105">DESCRIPTION</span></span>
<span data-ttu-id="607fd-106">Il cmdlet **Get-AzureRmStorageAccountKey** ottiene i tasti di scelta per un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="607fd-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="607fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="607fd-107">EXAMPLES</span></span>

### <span data-ttu-id="607fd-108">Esempio 1: ottenere i tasti di scelta per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="607fd-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="607fd-109">Questo comando consente di ottenere le chiavi per l'account di archiviazione di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="607fd-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="607fd-110">Esempio 2: ottenere un tasto di accesso specifico per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="607fd-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="607fd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="607fd-111">PARAMETERS</span></span>

### <span data-ttu-id="607fd-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="607fd-112">-Name</span></span>
<span data-ttu-id="607fd-113">Specifica il nome dell'account di archiviazione per cui questo cmdlet ottiene le chiavi.</span><span class="sxs-lookup"><span data-stu-id="607fd-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="607fd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607fd-114">-ResourceGroupName</span></span>
<span data-ttu-id="607fd-115">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="607fd-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="607fd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607fd-116">CommonParameters</span></span>
<span data-ttu-id="607fd-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607fd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607fd-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="607fd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607fd-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="607fd-119">INPUTS</span></span>

### <span data-ttu-id="607fd-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="607fd-120">None</span></span>
<span data-ttu-id="607fd-121">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="607fd-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="607fd-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="607fd-122">OUTPUTS</span></span>

## <span data-ttu-id="607fd-123">Note</span><span class="sxs-lookup"><span data-stu-id="607fd-123">NOTES</span></span>

## <span data-ttu-id="607fd-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="607fd-124">RELATED LINKS</span></span>

[<span data-ttu-id="607fd-125">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="607fd-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)

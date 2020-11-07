---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685599"
---
# <span data-ttu-id="bee3e-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="bee3e-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="bee3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bee3e-102">SYNOPSIS</span></span>
<span data-ttu-id="bee3e-103">Controlla la disponibilità di un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bee3e-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bee3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bee3e-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="bee3e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bee3e-105">DESCRIPTION</span></span>
<span data-ttu-id="bee3e-106">Il cmdlet **Get-AzureRmStorageAccountNameAvailability** controlla se il nome di un account di archiviazione di Azure è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="bee3e-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="bee3e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bee3e-107">EXAMPLES</span></span>

### <span data-ttu-id="bee3e-108">Esempio 1: verificare la disponibilità di un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="bee3e-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="bee3e-109">Questo comando controlla la disponibilità del nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="bee3e-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="bee3e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bee3e-110">PARAMETERS</span></span>

### <span data-ttu-id="bee3e-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="bee3e-111">-Name</span></span>
<span data-ttu-id="bee3e-112">Specifica il nome dell'account di archiviazione controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee3e-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="bee3e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee3e-113">CommonParameters</span></span>
<span data-ttu-id="bee3e-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee3e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee3e-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee3e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee3e-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bee3e-116">INPUTS</span></span>

### <span data-ttu-id="bee3e-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bee3e-117">None</span></span>
<span data-ttu-id="bee3e-118">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bee3e-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bee3e-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bee3e-119">OUTPUTS</span></span>

## <span data-ttu-id="bee3e-120">Note</span><span class="sxs-lookup"><span data-stu-id="bee3e-120">NOTES</span></span>

## <span data-ttu-id="bee3e-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bee3e-121">RELATED LINKS</span></span>

[<span data-ttu-id="bee3e-122">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="bee3e-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)

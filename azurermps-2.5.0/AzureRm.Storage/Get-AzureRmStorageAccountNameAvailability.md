---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
ms.openlocfilehash: 5371b5c54cfaff4b1c48dd8a8643e0cc51b1e00e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866183"
---
# <span data-ttu-id="7ce00-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7ce00-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="7ce00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ce00-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce00-103">Controlla la disponibilità di un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7ce00-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ce00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ce00-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ce00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ce00-105">DESCRIPTION</span></span>
<span data-ttu-id="7ce00-106">Il cmdlet **Get-AzureRmStorageAccountNameAvailability** controlla se il nome di un account di archiviazione di Azure è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="7ce00-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="7ce00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ce00-107">EXAMPLES</span></span>

### <span data-ttu-id="7ce00-108">Esempio 1: verificare la disponibilità di un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7ce00-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="7ce00-109">Questo comando controlla la disponibilità del nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="7ce00-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="7ce00-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ce00-110">PARAMETERS</span></span>

### <span data-ttu-id="7ce00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce00-111">-DefaultProfile</span></span>
<span data-ttu-id="7ce00-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ce00-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce00-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ce00-113">-Name</span></span>
<span data-ttu-id="7ce00-114">Specifica il nome dell'account di archiviazione controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ce00-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ce00-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce00-115">CommonParameters</span></span>
<span data-ttu-id="7ce00-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ce00-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce00-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ce00-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce00-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ce00-118">INPUTS</span></span>

### <span data-ttu-id="7ce00-119">System. String</span><span class="sxs-lookup"><span data-stu-id="7ce00-119">System.String</span></span>

## <span data-ttu-id="7ce00-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ce00-120">OUTPUTS</span></span>

### <span data-ttu-id="7ce00-121">Microsoft. Azure. Management. storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="7ce00-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="7ce00-122">Note</span><span class="sxs-lookup"><span data-stu-id="7ce00-122">NOTES</span></span>

## <span data-ttu-id="7ce00-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ce00-123">RELATED LINKS</span></span>

[<span data-ttu-id="7ce00-124">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="7ce00-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)



---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 402e3fdfe108486cd356af8a20ea06793f533937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520572"
---
# <span data-ttu-id="a87a1-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a87a1-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="a87a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a87a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a87a1-103">Controlla la disponibilità di un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a87a1-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a87a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a87a1-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a87a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a87a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a87a1-106">Il cmdlet **Get-AzureRmStorageAccountNameAvailability** controlla se il nome di un account di archiviazione di Azure è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="a87a1-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="a87a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a87a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a87a1-108">Esempio 1: verificare la disponibilità di un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a87a1-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="a87a1-109">Questo comando controlla la disponibilità del nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="a87a1-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="a87a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a87a1-110">PARAMETERS</span></span>

### <span data-ttu-id="a87a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a87a1-111">-DefaultProfile</span></span>
<span data-ttu-id="a87a1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a87a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a87a1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a87a1-113">-Name</span></span>
<span data-ttu-id="a87a1-114">Specifica il nome dell'account di archiviazione controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a87a1-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="a87a1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87a1-115">CommonParameters</span></span>
<span data-ttu-id="a87a1-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a87a1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87a1-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a87a1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87a1-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a87a1-118">INPUTS</span></span>

### <span data-ttu-id="a87a1-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a87a1-119">System.String</span></span>

## <span data-ttu-id="a87a1-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a87a1-120">OUTPUTS</span></span>

### <span data-ttu-id="a87a1-121">Microsoft. Azure. Management. storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="a87a1-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="a87a1-122">Note</span><span class="sxs-lookup"><span data-stu-id="a87a1-122">NOTES</span></span>

## <span data-ttu-id="a87a1-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a87a1-123">RELATED LINKS</span></span>

[<span data-ttu-id="a87a1-124">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="a87a1-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)



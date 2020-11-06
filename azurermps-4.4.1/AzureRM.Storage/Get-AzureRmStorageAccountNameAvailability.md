---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8ca5c33944882fde7e9bad2411df5f41dbe5f788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514640"
---
# <span data-ttu-id="63601-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="63601-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="63601-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63601-102">SYNOPSIS</span></span>
<span data-ttu-id="63601-103">Controlla la disponibilità di un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="63601-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63601-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63601-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63601-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63601-105">DESCRIPTION</span></span>
<span data-ttu-id="63601-106">Il cmdlet **Get-AzureRmStorageAccountNameAvailability** controlla se il nome di un account di archiviazione di Azure è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="63601-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="63601-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63601-107">EXAMPLES</span></span>

### <span data-ttu-id="63601-108">Esempio 1: verificare la disponibilità di un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="63601-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="63601-109">Questo comando controlla la disponibilità del nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="63601-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="63601-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63601-110">PARAMETERS</span></span>

### <span data-ttu-id="63601-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="63601-111">-Name</span></span>
<span data-ttu-id="63601-112">Specifica il nome dell'account di archiviazione controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63601-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="63601-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63601-113">-DefaultProfile</span></span>
<span data-ttu-id="63601-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63601-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63601-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63601-115">CommonParameters</span></span>
<span data-ttu-id="63601-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63601-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63601-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63601-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63601-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63601-118">INPUTS</span></span>

## <span data-ttu-id="63601-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63601-119">OUTPUTS</span></span>

## <span data-ttu-id="63601-120">Note</span><span class="sxs-lookup"><span data-stu-id="63601-120">NOTES</span></span>

## <span data-ttu-id="63601-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63601-121">RELATED LINKS</span></span>

[<span data-ttu-id="63601-122">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="63601-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)



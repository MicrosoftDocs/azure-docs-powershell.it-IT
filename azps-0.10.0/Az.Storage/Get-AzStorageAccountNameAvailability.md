---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 2000b2f50ac4c3c26f1e5dfbc5debe07ea9bd894
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862262"
---
# <span data-ttu-id="83897-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="83897-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="83897-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83897-102">SYNOPSIS</span></span>
<span data-ttu-id="83897-103">Controlla la disponibilità di un nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83897-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="83897-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83897-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83897-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83897-105">DESCRIPTION</span></span>
<span data-ttu-id="83897-106">Il cmdlet **Get-AzStorageAccountNameAvailability** controlla se il nome di un account di archiviazione di Azure è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="83897-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="83897-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83897-107">EXAMPLES</span></span>

### <span data-ttu-id="83897-108">Esempio 1: verificare la disponibilità di un nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="83897-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="83897-109">Questo comando controlla la disponibilità del nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="83897-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="83897-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83897-110">PARAMETERS</span></span>

### <span data-ttu-id="83897-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83897-111">-DefaultProfile</span></span>
<span data-ttu-id="83897-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83897-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83897-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="83897-113">-Name</span></span>
<span data-ttu-id="83897-114">Specifica il nome dell'account di archiviazione controllato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83897-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="83897-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83897-115">CommonParameters</span></span>
<span data-ttu-id="83897-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83897-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83897-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83897-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83897-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83897-118">INPUTS</span></span>

### <span data-ttu-id="83897-119">System. String</span><span class="sxs-lookup"><span data-stu-id="83897-119">System.String</span></span>

## <span data-ttu-id="83897-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83897-120">OUTPUTS</span></span>

### <span data-ttu-id="83897-121">Microsoft. Azure. Management. storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="83897-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="83897-122">Note</span><span class="sxs-lookup"><span data-stu-id="83897-122">NOTES</span></span>

## <span data-ttu-id="83897-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83897-123">RELATED LINKS</span></span>

[<span data-ttu-id="83897-124">Cmdlet di Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="83897-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)



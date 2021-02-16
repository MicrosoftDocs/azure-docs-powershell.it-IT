---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: c0b283c7645426af9397fd675fde825ff0b5f087
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201334"
---
# <span data-ttu-id="c4602-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="c4602-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="c4602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4602-102">SYNOPSIS</span></span>
<span data-ttu-id="c4602-103">Controlla la disponibilità di un nome di account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c4602-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="c4602-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4602-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4602-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4602-105">DESCRIPTION</span></span>
<span data-ttu-id="c4602-106">Il cmdlet **Get-AzStorageAccountNameAvailability** controlla se il nome di un account di archiviazione di Azure è valido e disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="c4602-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="c4602-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4602-107">EXAMPLES</span></span>

### <span data-ttu-id="c4602-108">Esempio 1: Verificare la disponibilità di un nome di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c4602-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="c4602-109">Questo comando verifica la disponibilità del nome ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="c4602-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="c4602-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4602-110">PARAMETERS</span></span>

### <span data-ttu-id="c4602-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4602-111">-DefaultProfile</span></span>
<span data-ttu-id="c4602-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4602-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4602-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c4602-113">-Name</span></span>
<span data-ttu-id="c4602-114">Specifica il nome dell'account di archiviazione verificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4602-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="c4602-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4602-115">CommonParameters</span></span>
<span data-ttu-id="c4602-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4602-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4602-117">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4602-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4602-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4602-118">INPUTS</span></span>

### <span data-ttu-id="c4602-119">System.String</span><span class="sxs-lookup"><span data-stu-id="c4602-119">System.String</span></span>

## <span data-ttu-id="c4602-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4602-120">OUTPUTS</span></span>

### <span data-ttu-id="c4602-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="c4602-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="c4602-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4602-122">NOTES</span></span>

## <span data-ttu-id="c4602-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4602-123">RELATED LINKS</span></span>

[<span data-ttu-id="c4602-124">Cmdlet di Gestione archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="c4602-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)



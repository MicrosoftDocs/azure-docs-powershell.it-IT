---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BF054CA4-B0A4-4BFC-A657-92A0D3ABBCB5
online version: ''
schema: 2.0.0
ms.openlocfilehash: f82db6a826a6ed612e1d98c7cef6ab642bf15858
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023509"
---
# <span data-ttu-id="d5fe6-101">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d5fe6-101">Get-AzureStorSimpleStorageAccountCredential</span></span>

## <span data-ttu-id="d5fe6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fe6-103">Ottiene le credenziali per gli account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-103">Gets credentials for storage accounts.</span></span>

## <span data-ttu-id="d5fe6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5fe6-104">SYNTAX</span></span>

```
Get-AzureStorSimpleStorageAccountCredential [-StorageAccountName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5fe6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fe6-106">Il cmdlet **Get-AzureStorSimpleStorageAccountCredential** ottiene le credenziali per gli account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-106">The **Get-AzureStorSimpleStorageAccountCredential** cmdlet gets credentials for storage accounts.</span></span>
<span data-ttu-id="d5fe6-107">Questo cmdlet ottiene tutti gli oggetti **StorageAccountCredential** configurati nel servizio o un **StorageAccountCredential** denominato.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-107">This cmdlet gets all **StorageAccountCredential** objects configured in the service or a named **StorageAccountCredential**.</span></span>

## <span data-ttu-id="d5fe6-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5fe6-108">EXAMPLES</span></span>

### <span data-ttu-id="d5fe6-109">Esempio 1: ottenere tutte le credenziali per una risorsa</span><span class="sxs-lookup"><span data-stu-id="d5fe6-109">Example 1: Get all credentials for a resource</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential
InstanceId                           Login           Name            UseSSL VolumeCount     CloudType    Location
----------                           -----           ----            ------ -----------     ---------    --------
b5e0857f-82ef-4426-883b-a612889ebee4 qwertyuiopa     AdminAccount    True   24              Azure
```

<span data-ttu-id="d5fe6-110">Questo comando consente di ottenere tutte le credenziali disponibili per gli account di archiviazione per la risorsa corrente.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-110">This command gets all available credentials for storage accounts for the current resource.</span></span>

### <span data-ttu-id="d5fe6-111">Esempio 2: ottenere le credenziali per un account di archiviazione specifico</span><span class="sxs-lookup"><span data-stu-id="d5fe6-111">Example 2: Get the credential for a specific storage account</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoCloudStorage"
VERBOSE: ClientRequestId: 16551af6-3398-4d30-a389-1b8eb01ce92c_PS
VERBOSE: ClientRequestId: 5041277d-4044-4b6c-ae19-4ea9e7ae135a_PS
VERBOSE: Storage Access Credential with name ContosoCloudStorage found! 


CloudType                        : Azure
Hostname                         : blob.core.windows.net
InstanceId                       : 8b3cb7bb-963b-4173-9598-52fe230b0350
IsDefault                        : False
Location                         : West US
Login                            : ContosoCloudStorage
Name                             : ContosoCloudStorage
OperationInProgress              : None
Password                         : 
PasswordEncryptionCertThumbprint : 
UseSSL                           : True
VolumeCount                      : 0
```

<span data-ttu-id="d5fe6-112">Questo comando ottiene le credenziali dell'account di archiviazione per l'account di archiviazione denominato ContosoCloudStorage.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-112">This command gets the storage account credential for the storage account named ContosoCloudStorage.</span></span>

## <span data-ttu-id="d5fe6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5fe6-113">PARAMETERS</span></span>

### <span data-ttu-id="d5fe6-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="d5fe6-114">-Profile</span></span>
<span data-ttu-id="d5fe6-115">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-115">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fe6-116">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5fe6-116">-StorageAccountName</span></span>
<span data-ttu-id="d5fe6-117">Specifica il nome dell'account di archiviazione per cui ottenere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-117">Specifies the name of the storage account for which to get credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fe6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fe6-118">CommonParameters</span></span>
<span data-ttu-id="d5fe6-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fe6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fe6-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fe6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fe6-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5fe6-121">INPUTS</span></span>

### <span data-ttu-id="d5fe6-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d5fe6-122">None</span></span>

## <span data-ttu-id="d5fe6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5fe6-123">OUTPUTS</span></span>

### <span data-ttu-id="d5fe6-124">StorageAccountCredential, IList\<StorageAccountCredential\></span><span class="sxs-lookup"><span data-stu-id="d5fe6-124">StorageAccountCredential, IList\<StorageAccountCredential\></span></span>
<span data-ttu-id="d5fe6-125">Questo cmdlet restituisce un oggetto **StorageAccountCredential** , se specifichi il parametro *StorageAccountName* o se non specifichi tale parametro, restituisce un oggetto **IList \<StorageAccountCredential\>** .</span><span class="sxs-lookup"><span data-stu-id="d5fe6-125">This cmdlet returns a **StorageAccountCredential** object, if you specify the *StorageAccountName* parameter, or if you do not specify that parameter, it returns an **IList\<StorageAccountCredential\>** object.</span></span>

## <span data-ttu-id="d5fe6-126">Note</span><span class="sxs-lookup"><span data-stu-id="d5fe6-126">NOTES</span></span>

## <span data-ttu-id="d5fe6-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5fe6-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5fe6-128">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d5fe6-128">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="d5fe6-129">Remove-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d5fe6-129">Remove-AzureStorSimpleStorageAccountCredential</span></span>](./Remove-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="d5fe6-130">Set-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d5fe6-130">Set-AzureStorSimpleStorageAccountCredential</span></span>](./Set-AzureStorSimpleStorageAccountCredential.md)



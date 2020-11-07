---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 0ec79b50d47a86b23e7c55e7277fe567ba46b9d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685963"
---
# <span data-ttu-id="78890-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="78890-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="78890-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78890-102">SYNOPSIS</span></span>
<span data-ttu-id="78890-103">Ottiene i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="78890-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78890-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78890-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78890-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78890-105">DESCRIPTION</span></span>
<span data-ttu-id="78890-106">Il cmdlet **Get-AzureStorageTableStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="78890-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="78890-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78890-107">EXAMPLES</span></span>

### <span data-ttu-id="78890-108">Esempio 1: ottenere un criterio di accesso archiviato in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="78890-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="78890-109">Questo comando consente di ottenere i criteri di accesso denominati Policy50 nella tabella di archiviazione denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="78890-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="78890-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="78890-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="78890-111">Questo comando consente di ottenere tutti i criteri di accesso nella tabella denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="78890-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="78890-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78890-112">PARAMETERS</span></span>

### <span data-ttu-id="78890-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="78890-113">-Context</span></span>
<span data-ttu-id="78890-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="78890-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="78890-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="78890-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78890-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78890-116">-DefaultProfile</span></span>
<span data-ttu-id="78890-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78890-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78890-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="78890-118">-Policy</span></span>
<span data-ttu-id="78890-119">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="78890-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78890-120">-Tabella</span><span class="sxs-lookup"><span data-stu-id="78890-120">-Table</span></span>
<span data-ttu-id="78890-121">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="78890-121">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78890-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78890-122">CommonParameters</span></span>
<span data-ttu-id="78890-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78890-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78890-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78890-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78890-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78890-125">INPUTS</span></span>

### <span data-ttu-id="78890-126">System. String</span><span class="sxs-lookup"><span data-stu-id="78890-126">System.String</span></span>

### <span data-ttu-id="78890-127">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="78890-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="78890-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78890-128">OUTPUTS</span></span>

### <span data-ttu-id="78890-129">Microsoft. WindowsAzure. storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="78890-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="78890-130">Note</span><span class="sxs-lookup"><span data-stu-id="78890-130">NOTES</span></span>

## <span data-ttu-id="78890-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78890-131">RELATED LINKS</span></span>

[<span data-ttu-id="78890-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="78890-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="78890-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="78890-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="78890-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="78890-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="78890-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="78890-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



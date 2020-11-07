---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 85501affef70ce0cf31e62f9083d5ed383425497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685543"
---
# <span data-ttu-id="dd3cd-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3cd-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="dd3cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd3cd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3cd-103">Ottiene i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd3cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd3cd-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd3cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd3cd-105">DESCRIPTION</span></span>
<span data-ttu-id="dd3cd-106">Il cmdlet **Get-AzureStorageTableStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="dd3cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd3cd-107">EXAMPLES</span></span>

### <span data-ttu-id="dd3cd-108">Esempio 1: ottenere un criterio di accesso archiviato in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dd3cd-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="dd3cd-109">Questo comando consente di ottenere i criteri di accesso denominati Policy50 nella tabella di archiviazione denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="dd3cd-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dd3cd-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="dd3cd-111">Questo comando consente di ottenere tutti i criteri di accesso nella tabella denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="dd3cd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd3cd-112">PARAMETERS</span></span>

### <span data-ttu-id="dd3cd-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="dd3cd-113">-Context</span></span>
<span data-ttu-id="dd3cd-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dd3cd-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd3cd-116">-Policy</span><span class="sxs-lookup"><span data-stu-id="dd3cd-116">-Policy</span></span>
<span data-ttu-id="dd3cd-117">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="dd3cd-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd3cd-118">-Tabella</span><span class="sxs-lookup"><span data-stu-id="dd3cd-118">-Table</span></span>
<span data-ttu-id="dd3cd-119">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-119">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd3cd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3cd-120">CommonParameters</span></span>
<span data-ttu-id="dd3cd-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd3cd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3cd-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd3cd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3cd-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd3cd-123">INPUTS</span></span>

### <span data-ttu-id="dd3cd-124">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd3cd-124">IStorageContext</span></span>

<span data-ttu-id="dd3cd-125">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="dd3cd-125">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="dd3cd-126">Stringa</span><span class="sxs-lookup"><span data-stu-id="dd3cd-126">String</span></span>

<span data-ttu-id="dd3cd-127">Il parametro "Table" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="dd3cd-127">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dd3cd-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd3cd-128">OUTPUTS</span></span>

### <span data-ttu-id="dd3cd-129">Microsoft. WindowsAzure. storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="dd3cd-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="dd3cd-130">Note</span><span class="sxs-lookup"><span data-stu-id="dd3cd-130">NOTES</span></span>

## <span data-ttu-id="dd3cd-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd3cd-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd3cd-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3cd-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd3cd-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3cd-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd3cd-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd3cd-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd3cd-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd3cd-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



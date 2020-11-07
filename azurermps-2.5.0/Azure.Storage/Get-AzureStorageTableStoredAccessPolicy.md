---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a9c141684eb924ed0b969c469214d92b847e13db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866606"
---
# <span data-ttu-id="b369d-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b369d-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b369d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b369d-102">SYNOPSIS</span></span>
<span data-ttu-id="b369d-103">Ottiene i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b369d-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b369d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b369d-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b369d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b369d-105">DESCRIPTION</span></span>
<span data-ttu-id="b369d-106">Il cmdlet **Get-AzureStorageTableStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b369d-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="b369d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b369d-107">EXAMPLES</span></span>

### <span data-ttu-id="b369d-108">Esempio 1: ottenere un criterio di accesso archiviato in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b369d-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="b369d-109">Questo comando consente di ottenere i criteri di accesso denominati Policy50 nella tabella di archiviazione denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="b369d-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="b369d-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b369d-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="b369d-111">Questo comando consente di ottenere tutti i criteri di accesso nella tabella denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="b369d-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="b369d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b369d-112">PARAMETERS</span></span>

### <span data-ttu-id="b369d-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b369d-113">-Context</span></span>
<span data-ttu-id="b369d-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b369d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b369d-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b369d-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b369d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b369d-116">-DefaultProfile</span></span>
<span data-ttu-id="b369d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b369d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b369d-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="b369d-118">-Policy</span></span>
<span data-ttu-id="b369d-119">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="b369d-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="b369d-120">-Tabella</span><span class="sxs-lookup"><span data-stu-id="b369d-120">-Table</span></span>
<span data-ttu-id="b369d-121">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b369d-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b369d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b369d-122">CommonParameters</span></span>
<span data-ttu-id="b369d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b369d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b369d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b369d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b369d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b369d-125">INPUTS</span></span>

### <span data-ttu-id="b369d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b369d-126">System.String</span></span>

### <span data-ttu-id="b369d-127">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b369d-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b369d-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b369d-128">OUTPUTS</span></span>

### <span data-ttu-id="b369d-129">Microsoft. WindowsAzure. storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="b369d-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="b369d-130">Note</span><span class="sxs-lookup"><span data-stu-id="b369d-130">NOTES</span></span>

## <span data-ttu-id="b369d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b369d-131">RELATED LINKS</span></span>

[<span data-ttu-id="b369d-132">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b369d-132">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b369d-133">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b369d-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b369d-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b369d-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b369d-135">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b369d-135">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



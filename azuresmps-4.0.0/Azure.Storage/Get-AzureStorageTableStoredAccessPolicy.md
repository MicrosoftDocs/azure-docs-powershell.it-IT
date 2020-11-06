---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8c22b3eb95ab940670043f9ae467663c951027d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507031"
---
# <span data-ttu-id="4c286-101">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c286-101">Get-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="4c286-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c286-102">SYNOPSIS</span></span>
<span data-ttu-id="4c286-103">Ottiene i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c286-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="4c286-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c286-104">SYNTAX</span></span>

```
Get-AzureStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c286-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c286-105">DESCRIPTION</span></span>
<span data-ttu-id="4c286-106">Il cmdlet **Get-AzureStorageTableStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c286-106">The **Get-AzureStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="4c286-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c286-107">EXAMPLES</span></span>

### <span data-ttu-id="4c286-108">Esempio 1: ottenere un criterio di accesso archiviato in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c286-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="4c286-109">Questo comando consente di ottenere i criteri di accesso denominati Policy50 nella tabella di archiviazione denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="4c286-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="4c286-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c286-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzureStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="4c286-111">Questo comando consente di ottenere tutti i criteri di accesso nella tabella denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="4c286-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="4c286-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c286-112">PARAMETERS</span></span>

### <span data-ttu-id="4c286-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4c286-113">-Context</span></span>
<span data-ttu-id="4c286-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c286-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4c286-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4c286-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4c286-116">-Policy</span><span class="sxs-lookup"><span data-stu-id="4c286-116">-Policy</span></span>
<span data-ttu-id="4c286-117">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="4c286-117">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="4c286-118">-Tabella</span><span class="sxs-lookup"><span data-stu-id="4c286-118">-Table</span></span>
<span data-ttu-id="4c286-119">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c286-119">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="4c286-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c286-120">CommonParameters</span></span>
<span data-ttu-id="4c286-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c286-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c286-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c286-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c286-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c286-123">INPUTS</span></span>

## <span data-ttu-id="4c286-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c286-124">OUTPUTS</span></span>

## <span data-ttu-id="4c286-125">Note</span><span class="sxs-lookup"><span data-stu-id="4c286-125">NOTES</span></span>

## <span data-ttu-id="4c286-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c286-126">RELATED LINKS</span></span>

[<span data-ttu-id="4c286-127">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c286-127">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4c286-128">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c286-128">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4c286-129">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c286-129">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4c286-130">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c286-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)



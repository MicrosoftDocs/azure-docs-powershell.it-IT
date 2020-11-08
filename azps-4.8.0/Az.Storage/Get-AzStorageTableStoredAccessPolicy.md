---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033636"
---
# <span data-ttu-id="1d293-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1d293-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="1d293-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d293-102">SYNOPSIS</span></span>
<span data-ttu-id="1d293-103">Ottiene i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d293-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="1d293-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d293-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d293-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d293-105">DESCRIPTION</span></span>
<span data-ttu-id="1d293-106">Il cmdlet **Get-AzStorageTableStoredAccessPolicy** elenca i criteri di accesso archiviati o i criteri per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d293-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="1d293-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d293-107">EXAMPLES</span></span>

### <span data-ttu-id="1d293-108">Esempio 1: ottenere un criterio di accesso archiviato in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1d293-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="1d293-109">Questo comando consente di ottenere i criteri di accesso denominati Policy50 nella tabella di archiviazione denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="1d293-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="1d293-110">Esempio 2: ottenere tutti i criteri di accesso archiviati in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1d293-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="1d293-111">Questo comando consente di ottenere tutti i criteri di accesso nella tabella denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="1d293-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="1d293-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d293-112">PARAMETERS</span></span>

### <span data-ttu-id="1d293-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1d293-113">-Context</span></span>
<span data-ttu-id="1d293-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d293-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1d293-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1d293-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1d293-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d293-116">-DefaultProfile</span></span>
<span data-ttu-id="1d293-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d293-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d293-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="1d293-118">-Policy</span></span>
<span data-ttu-id="1d293-119">Specifica un criterio di accesso archiviato, che include le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="1d293-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="1d293-120">-Tabella</span><span class="sxs-lookup"><span data-stu-id="1d293-120">-Table</span></span>
<span data-ttu-id="1d293-121">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d293-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="1d293-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d293-122">CommonParameters</span></span>
<span data-ttu-id="1d293-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d293-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d293-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d293-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d293-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d293-125">INPUTS</span></span>

### <span data-ttu-id="1d293-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1d293-126">System.String</span></span>

### <span data-ttu-id="1d293-127">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1d293-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1d293-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d293-128">OUTPUTS</span></span>

### <span data-ttu-id="1d293-129">Microsoft. WindowsAzure. storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="1d293-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="1d293-130">Note</span><span class="sxs-lookup"><span data-stu-id="1d293-130">NOTES</span></span>

## <span data-ttu-id="1d293-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d293-131">RELATED LINKS</span></span>

[<span data-ttu-id="1d293-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1d293-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1d293-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1d293-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1d293-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1d293-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1d293-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1d293-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)



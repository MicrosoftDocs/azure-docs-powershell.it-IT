---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: cf783e708f4e37de209681e65d19f51ea6aea80b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963518"
---
# <span data-ttu-id="d59c6-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d59c6-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d59c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d59c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d59c6-103">Crea criteri di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c6-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d59c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d59c6-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d59c6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d59c6-105">DESCRIPTION</span></span>
<span data-ttu-id="d59c6-106">Il cmdlet **New-AzStorageTableStoredAccessPolicy** crea un criterio di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c6-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d59c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d59c6-107">EXAMPLES</span></span>

### <span data-ttu-id="d59c6-108">Esempio 1: Creare criteri di accesso archiviati in una tabella</span><span class="sxs-lookup"><span data-stu-id="d59c6-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="d59c6-109">Questo comando crea un criterio di accesso denominato Criterio02 nella tabella di archiviazione denominata Tabella_</span><span class="sxs-lookup"><span data-stu-id="d59c6-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="d59c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d59c6-110">PARAMETERS</span></span>

### <span data-ttu-id="d59c6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d59c6-111">-Context</span></span>
<span data-ttu-id="d59c6-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d59c6-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d59c6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d59c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59c6-114">-DefaultProfile</span></span>
<span data-ttu-id="d59c6-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d59c6-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d59c6-116">-ExpiryTime</span></span>
<span data-ttu-id="d59c6-117">Specifica l'ora in cui i criteri di accesso archiviato non sono più validi.</span><span class="sxs-lookup"><span data-stu-id="d59c6-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59c6-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="d59c6-118">-Permission</span></span>
<span data-ttu-id="d59c6-119">Specifica le autorizzazioni nei criteri di accesso archiviato per accedere alla tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d59c6-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="d59c6-120">È importante notare che si tratta di una stringa, ad esempio `raud` (per Lettura, Aggiungi, Aggiorna ed Elimina).</span><span class="sxs-lookup"><span data-stu-id="d59c6-120">It is important to note that this is a string, like `raud` (for Read, Add, Update and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59c6-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="d59c6-121">-Policy</span></span>
<span data-ttu-id="d59c6-122">Specifica un nome per i criteri di accesso archiviato.</span><span class="sxs-lookup"><span data-stu-id="d59c6-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59c6-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d59c6-123">-StartTime</span></span>
<span data-ttu-id="d59c6-124">Specifica l'ora in cui i criteri di accesso archiviato diventano validi.</span><span class="sxs-lookup"><span data-stu-id="d59c6-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59c6-125">-Table</span><span class="sxs-lookup"><span data-stu-id="d59c6-125">-Table</span></span>
<span data-ttu-id="d59c6-126">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c6-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="d59c6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59c6-127">CommonParameters</span></span>
<span data-ttu-id="d59c6-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59c6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59c6-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59c6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59c6-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="d59c6-130">INPUTS</span></span>

### <span data-ttu-id="d59c6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d59c6-131">System.String</span></span>

### <span data-ttu-id="d59c6-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d59c6-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d59c6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d59c6-133">OUTPUTS</span></span>

### <span data-ttu-id="d59c6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d59c6-134">System.String</span></span>

## <span data-ttu-id="d59c6-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d59c6-135">NOTES</span></span>

## <span data-ttu-id="d59c6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d59c6-136">RELATED LINKS</span></span>

[<span data-ttu-id="d59c6-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d59c6-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d59c6-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d59c6-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d59c6-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d59c6-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d59c6-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d59c6-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)



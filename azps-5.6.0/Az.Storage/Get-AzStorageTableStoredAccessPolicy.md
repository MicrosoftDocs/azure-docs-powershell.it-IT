---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994782"
---
# <span data-ttu-id="30047-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30047-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="30047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30047-102">SYNOPSIS</span></span>
<span data-ttu-id="30047-103">Recupera i criteri di accesso archiviati per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="30047-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="30047-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30047-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30047-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30047-105">DESCRIPTION</span></span>
<span data-ttu-id="30047-106">Il cmdlet **Get-AzStorageTableStoredAccessPolicy** elenca i criteri di accesso archiviato per una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="30047-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="30047-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30047-107">EXAMPLES</span></span>

### <span data-ttu-id="30047-108">Esempio 1: Ottenere criteri di accesso archiviato in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="30047-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="30047-109">Questo comando recupera i criteri di accesso denominati Policy50 nella tabella di archiviazione denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="30047-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="30047-110">Esempio 2: Ottenere tutti i criteri di accesso archiviato in una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="30047-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="30047-111">Questo comando recupera tutti i criteri di accesso nella tabella denominata Table02.</span><span class="sxs-lookup"><span data-stu-id="30047-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="30047-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30047-112">PARAMETERS</span></span>

### <span data-ttu-id="30047-113">-Context</span><span class="sxs-lookup"><span data-stu-id="30047-113">-Context</span></span>
<span data-ttu-id="30047-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="30047-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="30047-115">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="30047-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="30047-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30047-116">-DefaultProfile</span></span>
<span data-ttu-id="30047-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30047-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30047-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="30047-118">-Policy</span></span>
<span data-ttu-id="30047-119">Specifica i criteri di accesso archiviato, che includono le autorizzazioni per questo token di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="30047-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="30047-120">-Table</span><span class="sxs-lookup"><span data-stu-id="30047-120">-Table</span></span>
<span data-ttu-id="30047-121">Specifica il nome della tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="30047-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="30047-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30047-122">CommonParameters</span></span>
<span data-ttu-id="30047-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30047-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30047-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30047-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30047-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="30047-125">INPUTS</span></span>

### <span data-ttu-id="30047-126">System.String</span><span class="sxs-lookup"><span data-stu-id="30047-126">System.String</span></span>

### <span data-ttu-id="30047-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="30047-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="30047-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30047-128">OUTPUTS</span></span>

### <span data-ttu-id="30047-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="30047-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="30047-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="30047-130">NOTES</span></span>

## <span data-ttu-id="30047-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30047-131">RELATED LINKS</span></span>

[<span data-ttu-id="30047-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30047-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="30047-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30047-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="30047-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30047-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="30047-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="30047-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)



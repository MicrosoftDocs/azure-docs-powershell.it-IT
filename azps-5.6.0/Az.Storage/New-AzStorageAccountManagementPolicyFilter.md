---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 40a2420803197b21bb9f0f8d20b771482b4e694b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002637"
---
# <span data-ttu-id="bec0f-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="bec0f-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="bec0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec0f-102">SYNOPSIS</span></span>
<span data-ttu-id="bec0f-103">Crea un oggetto filtro regola ManagementPolicy, che può essere usato in New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="bec0f-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="bec0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bec0f-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-BlobType <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bec0f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bec0f-105">DESCRIPTION</span></span>
<span data-ttu-id="bec0f-106">Il cmdlet **New-AzStorageAccountManagementPolicyFilter** crea un oggetto filtro della regola ManagementPolicy, che può essere usato in New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="bec0f-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="bec0f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bec0f-107">EXAMPLES</span></span>

### <span data-ttu-id="bec0f-108">Esempio 1: crea un oggetto filtro della regola ManagementPolicy, quindi lo aggiunge a una regola dei criteri di gestione e impostato su un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="bec0f-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2 -BlobType appendBlob,blockBlob
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {appendBlob, blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="bec0f-109">Questo comando crea un oggetto filtro regola ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="bec0f-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="bec0f-110">Quindi aggiungerla a una regola dei criteri di gestione e impostarla su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bec0f-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="bec0f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bec0f-111">PARAMETERS</span></span>

### <span data-ttu-id="bec0f-112">-BLOBType</span><span class="sxs-lookup"><span data-stu-id="bec0f-112">-BlobType</span></span>
<span data-ttu-id="bec0f-113">Matrice di stringhe in cui trovare corrispondenze per i tipi di BLOB.</span><span class="sxs-lookup"><span data-stu-id="bec0f-113">An array of strings for blobtypes to be match.</span></span> <span data-ttu-id="bec0f-114">Attualmente blockBlob supporta tutte le azioni di eliminazione e livelli.</span><span class="sxs-lookup"><span data-stu-id="bec0f-114">Currently blockBlob supports all tiering and delete actions.</span></span> <span data-ttu-id="bec0f-115">Solo le azioni di eliminazione sono supportate per appendBlob.</span><span class="sxs-lookup"><span data-stu-id="bec0f-115">Only delete actions are supported for appendBlob.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: blockBlob, appendBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec0f-116">-DefaultProfile</span></span>
<span data-ttu-id="bec0f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bec0f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec0f-118">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="bec0f-118">-PrefixMatch</span></span>
<span data-ttu-id="bec0f-119">Matrice di stringhe per i prefissi che devono essere corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="bec0f-119">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="bec0f-120">Una stringa di prefisso deve iniziare con un nome di contenitore.</span><span class="sxs-lookup"><span data-stu-id="bec0f-120">A prefix string must start with a container name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec0f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec0f-121">CommonParameters</span></span>
<span data-ttu-id="bec0f-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec0f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec0f-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec0f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec0f-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="bec0f-124">INPUTS</span></span>

### <span data-ttu-id="bec0f-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bec0f-125">None</span></span>

## <span data-ttu-id="bec0f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bec0f-126">OUTPUTS</span></span>

### <span data-ttu-id="bec0f-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="bec0f-127">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="bec0f-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="bec0f-128">NOTES</span></span>

## <span data-ttu-id="bec0f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bec0f-129">RELATED LINKS</span></span>

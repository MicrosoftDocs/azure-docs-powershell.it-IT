---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 48ae8b87671e52abe4d109025048fe1e4aeca117
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476051"
---
# <span data-ttu-id="d2ec0-101">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="d2ec0-101">New-AzStorageAccountManagementPolicyFilter</span></span>

## <span data-ttu-id="d2ec0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ec0-103">Crea un oggetto filtro di regola ManagementPolicy, che può essere usato in New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-103">Creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="d2ec0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2ec0-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2ec0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ec0-106">Il cmdlet **New-AzStorageAccountManagementPolicyFilter** crea un oggetto Filter di ManagementPolicy Rule, che può essere usato in New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-106">The **New-AzStorageAccountManagementPolicyFilter** cmdlet creates a ManagementPolicy rule filter object, which can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="d2ec0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2ec0-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ec0-108">Esempio 1: crea un oggetto filtro di regola ManagementPolicy, quindi aggiungilo a una regola di criteri di gestione e impostato su un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d2ec0-108">Example 1: Creates a ManagementPolicy rule filter object, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="d2ec0-109">Questo comando crea un oggetto filtro di regola ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-109">This command create a ManagementPolicy rule filter object.</span></span> <span data-ttu-id="d2ec0-110">Quindi aggiungilo a una regola di criteri di gestione e impostalo su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-110">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="d2ec0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2ec0-111">PARAMETERS</span></span>

### <span data-ttu-id="d2ec0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ec0-112">-DefaultProfile</span></span>
<span data-ttu-id="d2ec0-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ec0-114">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="d2ec0-114">-PrefixMatch</span></span>
<span data-ttu-id="d2ec0-115">Matrice di stringhe per i prefissi da corrispondere.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-115">An array of strings for prefixes to be match.</span></span>
<span data-ttu-id="d2ec0-116">Una stringa di prefisso deve iniziare con il nome di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-116">A prefix string must start with a container name.</span></span>

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

### <span data-ttu-id="d2ec0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ec0-117">CommonParameters</span></span>
<span data-ttu-id="d2ec0-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ec0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ec0-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ec0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ec0-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2ec0-120">INPUTS</span></span>

### <span data-ttu-id="d2ec0-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d2ec0-121">None</span></span>

## <span data-ttu-id="d2ec0-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2ec0-122">OUTPUTS</span></span>

### <span data-ttu-id="d2ec0-123">Microsoft. Azure. Commands. Management. storage. Models. PSManagementPolicyRuleFilter</span><span class="sxs-lookup"><span data-stu-id="d2ec0-123">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter</span></span>

## <span data-ttu-id="d2ec0-124">Note</span><span class="sxs-lookup"><span data-stu-id="d2ec0-124">NOTES</span></span>

## <span data-ttu-id="d2ec0-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2ec0-125">RELATED LINKS</span></span>

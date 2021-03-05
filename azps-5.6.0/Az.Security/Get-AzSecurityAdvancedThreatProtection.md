---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ec35304bf6c376747fa6f98e7fb5753293e579b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008557"
---
# <span data-ttu-id="4cdf2-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4cdf2-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="4cdf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cdf2-102">SYNOPSIS</span></span>
<span data-ttu-id="4cdf2-103">Ottiene i criteri di protezione avanzata dalle minacce per un account di archiviazione/database.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="4cdf2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4cdf2-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cdf2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4cdf2-105">DESCRIPTION</span></span>
<span data-ttu-id="4cdf2-106">Il `Get-AzSecurityAdvancedThreatProtection` cmdlet ottiene i criteri di protezione dalle minacce per un account di archiviazione/database.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="4cdf2-107">Per usare questo cmdlet, specificare il *parametro ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="4cdf2-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="4cdf2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4cdf2-108">EXAMPLES</span></span>

### <span data-ttu-id="4cdf2-109">Esempio 1: Account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4cdf2-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="4cdf2-110">Questo comando ottiene i criteri di Protezione avanzata dalle minacce per l'ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` risorsa.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="4cdf2-111">Esempio 2: Account AMMORT personale</span><span class="sxs-lookup"><span data-stu-id="4cdf2-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="4cdf2-112">Questo comando ottiene i criteri di Protezione avanzata dalle minacce per l'ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` risorsa.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="4cdf2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cdf2-113">PARAMETERS</span></span>

### <span data-ttu-id="4cdf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cdf2-114">-DefaultProfile</span></span>
<span data-ttu-id="4cdf2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cdf2-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cdf2-116">-ResourceId</span></span>
<span data-ttu-id="4cdf2-117">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cdf2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cdf2-118">CommonParameters</span></span>
<span data-ttu-id="4cdf2-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cdf2-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cdf2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cdf2-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="4cdf2-121">INPUTS</span></span>

### <span data-ttu-id="4cdf2-122">System.String</span><span class="sxs-lookup"><span data-stu-id="4cdf2-122">System.String</span></span>

## <span data-ttu-id="4cdf2-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4cdf2-123">OUTPUTS</span></span>

### <span data-ttu-id="4cdf2-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="4cdf2-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="4cdf2-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="4cdf2-125">NOTES</span></span>

## <span data-ttu-id="4cdf2-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4cdf2-126">RELATED LINKS</span></span>

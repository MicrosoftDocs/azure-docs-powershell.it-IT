---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188254"
---
# <span data-ttu-id="136f4-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="136f4-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="136f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="136f4-102">SYNOPSIS</span></span>
<span data-ttu-id="136f4-103">Ottiene i criteri avanzati per la protezione delle minacce per un account di archiviazione/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="136f4-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="136f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="136f4-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="136f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="136f4-105">DESCRIPTION</span></span>
<span data-ttu-id="136f4-106">Il `Get-AzSecurityAdvancedThreatProtection` cmdlet ottiene i criteri di protezione dalle minacce per un account di archiviazione/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="136f4-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="136f4-107">Per usare questo cmdlet, specifica il parametro *resourceId* .</span><span class="sxs-lookup"><span data-stu-id="136f4-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="136f4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="136f4-108">EXAMPLES</span></span>

### <span data-ttu-id="136f4-109">Esempio 1: account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="136f4-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="136f4-110">Questo comando ottiene i criteri avanzati per la protezione delle minacce per l'ID risorsa `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="136f4-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="136f4-111">Esempio 2: account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="136f4-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="136f4-112">Questo comando ottiene i criteri avanzati per la protezione delle minacce per l'ID risorsa ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="136f4-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="136f4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="136f4-113">PARAMETERS</span></span>

### <span data-ttu-id="136f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136f4-114">-DefaultProfile</span></span>
<span data-ttu-id="136f4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="136f4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="136f4-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="136f4-116">-ResourceId</span></span>
<span data-ttu-id="136f4-117">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="136f4-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="136f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136f4-118">CommonParameters</span></span>
<span data-ttu-id="136f4-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="136f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136f4-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="136f4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136f4-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="136f4-121">INPUTS</span></span>

### <span data-ttu-id="136f4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="136f4-122">System.String</span></span>

## <span data-ttu-id="136f4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="136f4-123">OUTPUTS</span></span>

### <span data-ttu-id="136f4-124">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="136f4-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="136f4-125">Note</span><span class="sxs-lookup"><span data-stu-id="136f4-125">NOTES</span></span>

## <span data-ttu-id="136f4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="136f4-126">RELATED LINKS</span></span>

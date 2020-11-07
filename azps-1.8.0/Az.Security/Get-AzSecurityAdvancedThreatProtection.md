---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677216"
---
# <span data-ttu-id="7eff5-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="7eff5-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="7eff5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7eff5-102">SYNOPSIS</span></span>
<span data-ttu-id="7eff5-103">Ottiene i criteri avanzati per la protezione delle minacce per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7eff5-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="7eff5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7eff5-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eff5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7eff5-105">DESCRIPTION</span></span>
<span data-ttu-id="7eff5-106">Il `Get-AzSecurityAdvancedThreatProtection` cmdlet ottiene i criteri di protezione dalle minacce per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7eff5-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="7eff5-107">Per usare questo cmdlet, specifica il parametro *resourceId* .</span><span class="sxs-lookup"><span data-stu-id="7eff5-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="7eff5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7eff5-108">EXAMPLES</span></span>

### <span data-ttu-id="7eff5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7eff5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="7eff5-110">Questo comando ottiene i criteri avanzati per la protezione delle minacce per l'ID risorsa `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="7eff5-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="7eff5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7eff5-111">PARAMETERS</span></span>

### <span data-ttu-id="7eff5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eff5-112">-DefaultProfile</span></span>
<span data-ttu-id="7eff5-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7eff5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eff5-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eff5-114">-ResourceId</span></span>
<span data-ttu-id="7eff5-115">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="7eff5-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="7eff5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eff5-116">CommonParameters</span></span>
<span data-ttu-id="7eff5-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eff5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eff5-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eff5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eff5-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7eff5-119">INPUTS</span></span>

### <span data-ttu-id="7eff5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7eff5-120">System.String</span></span>

## <span data-ttu-id="7eff5-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7eff5-121">OUTPUTS</span></span>

### <span data-ttu-id="7eff5-122">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="7eff5-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="7eff5-123">Note</span><span class="sxs-lookup"><span data-stu-id="7eff5-123">NOTES</span></span>

## <span data-ttu-id="7eff5-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7eff5-124">RELATED LINKS</span></span>

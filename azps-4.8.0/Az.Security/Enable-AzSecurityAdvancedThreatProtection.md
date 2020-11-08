---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191951"
---
# <span data-ttu-id="14aef-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="14aef-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="14aef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14aef-102">SYNOPSIS</span></span>
<span data-ttu-id="14aef-103">Abilita i criteri avanzati per la protezione delle minacce per un account di archiviazione/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="14aef-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="14aef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14aef-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14aef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14aef-105">DESCRIPTION</span></span>
<span data-ttu-id="14aef-106">Il `Enable-AzSecurityAdvancedThreatProtection` cmdlet Abilita i criteri di protezione dalle minacce per un account di archiviazione/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="14aef-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="14aef-107">Per usare questo cmdlet, specifica il parametro *resourceId* .</span><span class="sxs-lookup"><span data-stu-id="14aef-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="14aef-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14aef-108">EXAMPLES</span></span>

### <span data-ttu-id="14aef-109">Esempio 1: account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="14aef-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="14aef-110">Questo comando Abilita i criteri avanzati per la protezione delle minacce per l'ID risorsa `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="14aef-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="14aef-111">Esempio 2: account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="14aef-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="14aef-112">Questo comando Abilita i criteri avanzati per la protezione delle minacce per l'ID risorsa ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="14aef-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="14aef-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14aef-113">PARAMETERS</span></span>

### <span data-ttu-id="14aef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14aef-114">-DefaultProfile</span></span>
<span data-ttu-id="14aef-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14aef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14aef-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14aef-116">-ResourceId</span></span>
<span data-ttu-id="14aef-117">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="14aef-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="14aef-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14aef-118">-Confirm</span></span>
<span data-ttu-id="14aef-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14aef-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14aef-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14aef-120">-WhatIf</span></span>
<span data-ttu-id="14aef-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14aef-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14aef-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14aef-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14aef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14aef-123">CommonParameters</span></span>
<span data-ttu-id="14aef-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14aef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14aef-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14aef-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14aef-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14aef-126">INPUTS</span></span>

### <span data-ttu-id="14aef-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14aef-127">None</span></span>

## <span data-ttu-id="14aef-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14aef-128">OUTPUTS</span></span>

### <span data-ttu-id="14aef-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="14aef-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="14aef-130">Note</span><span class="sxs-lookup"><span data-stu-id="14aef-130">NOTES</span></span>

## <span data-ttu-id="14aef-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14aef-131">RELATED LINKS</span></span>
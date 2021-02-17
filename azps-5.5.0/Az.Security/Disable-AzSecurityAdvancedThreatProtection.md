---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e7195131830fd5b19a6d67b4fae5583374da7d0f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178654"
---
# <span data-ttu-id="ec83e-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ec83e-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="ec83e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec83e-102">SYNOPSIS</span></span>
<span data-ttu-id="ec83e-103">Disabilita i criteri di protezione avanzata dalle minacce per un account di archiviazione/database.</span><span class="sxs-lookup"><span data-stu-id="ec83e-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="ec83e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec83e-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec83e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ec83e-105">DESCRIPTION</span></span>
<span data-ttu-id="ec83e-106">Il `Disable-AzSecurityAdvancedThreatProtection` cmdlet disabilita i criteri di protezione dalle minacce per un account di archiviazione/database.</span><span class="sxs-lookup"><span data-stu-id="ec83e-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="ec83e-107">Per usare questo cmdlet, specificare il *parametro ResourceId.*</span><span class="sxs-lookup"><span data-stu-id="ec83e-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="ec83e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec83e-108">EXAMPLES</span></span>

### <span data-ttu-id="ec83e-109">Esempio 1: Account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ec83e-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="ec83e-110">Questo comando disabilita i criteri di Protezione avanzata dalle minacce per l'ID `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec83e-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="ec83e-111">Esempio 2 : Account Database Bancario</span><span class="sxs-lookup"><span data-stu-id="ec83e-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="ec83e-112">Questo comando disabilita i criteri di Protezione avanzata dalle minacce per l'ID ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` risorsa.</span><span class="sxs-lookup"><span data-stu-id="ec83e-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="ec83e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec83e-113">PARAMETERS</span></span>

### <span data-ttu-id="ec83e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec83e-114">-DefaultProfile</span></span>
<span data-ttu-id="ec83e-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec83e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec83e-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec83e-116">-ResourceId</span></span>
<span data-ttu-id="ec83e-117">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="ec83e-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ec83e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec83e-118">-Confirm</span></span>
<span data-ttu-id="ec83e-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec83e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec83e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec83e-120">-WhatIf</span></span>
<span data-ttu-id="ec83e-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec83e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec83e-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec83e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec83e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec83e-123">CommonParameters</span></span>
<span data-ttu-id="ec83e-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec83e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec83e-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ec83e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec83e-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="ec83e-126">INPUTS</span></span>

### <span data-ttu-id="ec83e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ec83e-127">None</span></span>

## <span data-ttu-id="ec83e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec83e-128">OUTPUTS</span></span>

### <span data-ttu-id="ec83e-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ec83e-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="ec83e-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="ec83e-130">NOTES</span></span>

## <span data-ttu-id="ec83e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec83e-131">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: c2d2bcaf95b7eda010cc299a7c20cfd703f7eadb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854730"
---
# <span data-ttu-id="31033-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="31033-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="31033-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31033-102">SYNOPSIS</span></span>
<span data-ttu-id="31033-103">Disabilita i criteri avanzati per la protezione delle minacce per un account di archiviazione/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="31033-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="31033-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31033-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31033-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31033-105">DESCRIPTION</span></span>
<span data-ttu-id="31033-106">Il `Disable-AzSecurityAdvancedThreatProtection` cmdlet Disabilita i criteri di protezione dalle minacce per un account di archiviazione/cosmosDB.</span><span class="sxs-lookup"><span data-stu-id="31033-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="31033-107">Per usare questo cmdlet, specifica il parametro *resourceId* .</span><span class="sxs-lookup"><span data-stu-id="31033-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="31033-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31033-108">EXAMPLES</span></span>

### <span data-ttu-id="31033-109">Esempio 1: account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="31033-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="31033-110">Questo comando Disabilita i criteri avanzati per la protezione delle minacce per l'ID risorsa `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="31033-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="31033-111">Esempio 2: account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="31033-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="31033-112">Questo comando Disabilita i criteri avanzati per la protezione delle minacce per l'ID risorsa ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="31033-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="31033-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31033-113">PARAMETERS</span></span>

### <span data-ttu-id="31033-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31033-114">-DefaultProfile</span></span>
<span data-ttu-id="31033-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31033-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31033-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31033-116">-ResourceId</span></span>
<span data-ttu-id="31033-117">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="31033-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="31033-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31033-118">-Confirm</span></span>
<span data-ttu-id="31033-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31033-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31033-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31033-120">-WhatIf</span></span>
<span data-ttu-id="31033-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31033-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31033-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31033-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31033-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31033-123">CommonParameters</span></span>
<span data-ttu-id="31033-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31033-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31033-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31033-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31033-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31033-126">INPUTS</span></span>

### <span data-ttu-id="31033-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="31033-127">None</span></span>

## <span data-ttu-id="31033-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31033-128">OUTPUTS</span></span>

### <span data-ttu-id="31033-129">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="31033-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="31033-130">Note</span><span class="sxs-lookup"><span data-stu-id="31033-130">NOTES</span></span>

## <span data-ttu-id="31033-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31033-131">RELATED LINKS</span></span>

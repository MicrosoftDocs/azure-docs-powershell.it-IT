---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: a3e83b4c58a7de2a0c020bc156e78656a6fd75ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677223"
---
# <span data-ttu-id="46535-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="46535-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="46535-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46535-102">SYNOPSIS</span></span>
<span data-ttu-id="46535-103">Disabilita i criteri avanzati per la protezione delle minacce per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="46535-103">Disables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="46535-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46535-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46535-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46535-105">DESCRIPTION</span></span>
<span data-ttu-id="46535-106">Il `Disable-AzSecurityAdvancedThreatProtection` cmdlet Disabilita i criteri di protetion della minaccia per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="46535-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="46535-107">Per usare questo cmdlet, specifica il parametro *resourceId* .</span><span class="sxs-lookup"><span data-stu-id="46535-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="46535-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46535-108">EXAMPLES</span></span>

### <span data-ttu-id="46535-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46535-109">Example 1</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="46535-110">Questo comando Disabilita i criteri avanzati per la protezione delle minacce per l'ID risorsa `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="46535-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="46535-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46535-111">PARAMETERS</span></span>

### <span data-ttu-id="46535-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46535-112">-DefaultProfile</span></span>
<span data-ttu-id="46535-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46535-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46535-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46535-114">-ResourceId</span></span>
<span data-ttu-id="46535-115">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="46535-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="46535-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46535-116">-Confirm</span></span>
<span data-ttu-id="46535-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46535-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46535-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46535-118">-WhatIf</span></span>
<span data-ttu-id="46535-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46535-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46535-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46535-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46535-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46535-121">CommonParameters</span></span>
<span data-ttu-id="46535-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46535-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46535-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46535-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46535-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46535-124">INPUTS</span></span>

### <span data-ttu-id="46535-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="46535-125">None</span></span>

## <span data-ttu-id="46535-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46535-126">OUTPUTS</span></span>

### <span data-ttu-id="46535-127">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="46535-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="46535-128">Note</span><span class="sxs-lookup"><span data-stu-id="46535-128">NOTES</span></span>

## <span data-ttu-id="46535-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46535-129">RELATED LINKS</span></span>

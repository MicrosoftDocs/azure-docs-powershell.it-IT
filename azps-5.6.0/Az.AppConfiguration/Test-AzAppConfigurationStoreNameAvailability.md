---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: 87d19475896138ee51a31694f707c1839f839ba8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963310"
---
# <span data-ttu-id="ba6bb-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ba6bb-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="ba6bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6bb-103">Controlla se il nome dell'archivio di configurazione è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ba6bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba6bb-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba6bb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba6bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ba6bb-106">Controlla se il nome dell'archivio di configurazione è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="ba6bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba6bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ba6bb-108">Esempio 1: Verificare la disponibilità del nome dell'app configuration store</span><span class="sxs-lookup"><span data-stu-id="ba6bb-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="ba6bb-109">Questo comando verifica la disponibilità del nome dell'archivio di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="ba6bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba6bb-110">PARAMETERS</span></span>

### <span data-ttu-id="ba6bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6bb-111">-DefaultProfile</span></span>
<span data-ttu-id="ba6bb-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6bb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ba6bb-113">-Name</span></span>
<span data-ttu-id="ba6bb-114">Nome da assegnare alla verifica della disponibilità.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-114">The name to check for availability.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6bb-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba6bb-115">-SubscriptionId</span></span>
<span data-ttu-id="ba6bb-116">ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6bb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba6bb-117">-Confirm</span></span>
<span data-ttu-id="ba6bb-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba6bb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba6bb-119">-WhatIf</span></span>
<span data-ttu-id="ba6bb-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba6bb-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba6bb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6bb-122">CommonParameters</span></span>
<span data-ttu-id="ba6bb-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6bb-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ba6bb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6bb-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba6bb-125">INPUTS</span></span>

## <span data-ttu-id="ba6bb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba6bb-126">OUTPUTS</span></span>

### <span data-ttu-id="ba6bb-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ba6bb-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="ba6bb-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba6bb-128">NOTES</span></span>

<span data-ttu-id="ba6bb-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ba6bb-129">ALIASES</span></span>

## <span data-ttu-id="ba6bb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba6bb-130">RELATED LINKS</span></span>


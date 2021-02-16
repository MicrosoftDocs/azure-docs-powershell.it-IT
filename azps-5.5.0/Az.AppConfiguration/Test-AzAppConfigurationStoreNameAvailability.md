---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195327"
---
# <span data-ttu-id="489cd-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="489cd-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="489cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="489cd-102">SYNOPSIS</span></span>
<span data-ttu-id="489cd-103">Controlla se il nome dell'archivio di configurazione è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="489cd-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="489cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="489cd-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="489cd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="489cd-105">DESCRIPTION</span></span>
<span data-ttu-id="489cd-106">Controlla se il nome dell'archivio di configurazione è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="489cd-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="489cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="489cd-107">EXAMPLES</span></span>

### <span data-ttu-id="489cd-108">Esempio 1: Verificare la disponibilità del nome dell'app configuration store</span><span class="sxs-lookup"><span data-stu-id="489cd-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="489cd-109">Questo comando verifica la disponibilità del nome dell'archivio della configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="489cd-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="489cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="489cd-110">PARAMETERS</span></span>

### <span data-ttu-id="489cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="489cd-111">-DefaultProfile</span></span>
<span data-ttu-id="489cd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="489cd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="489cd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="489cd-113">-Name</span></span>
<span data-ttu-id="489cd-114">Nome da assegnare alla verifica della disponibilità.</span><span class="sxs-lookup"><span data-stu-id="489cd-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="489cd-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="489cd-115">-SubscriptionId</span></span>
<span data-ttu-id="489cd-116">ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="489cd-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="489cd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="489cd-117">-Confirm</span></span>
<span data-ttu-id="489cd-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="489cd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="489cd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="489cd-119">-WhatIf</span></span>
<span data-ttu-id="489cd-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="489cd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="489cd-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="489cd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="489cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="489cd-122">CommonParameters</span></span>
<span data-ttu-id="489cd-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="489cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="489cd-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="489cd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="489cd-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="489cd-125">INPUTS</span></span>

## <span data-ttu-id="489cd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="489cd-126">OUTPUTS</span></span>

### <span data-ttu-id="489cd-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="489cd-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="489cd-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="489cd-128">NOTES</span></span>

<span data-ttu-id="489cd-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="489cd-129">ALIASES</span></span>

## <span data-ttu-id="489cd-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="489cd-130">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381454"
---
# <span data-ttu-id="2992f-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2992f-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="2992f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2992f-102">SYNOPSIS</span></span>
<span data-ttu-id="2992f-103">Controlla se il nome dell'archivio configurazione è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="2992f-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="2992f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2992f-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2992f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2992f-105">DESCRIPTION</span></span>
<span data-ttu-id="2992f-106">Controlla se il nome dell'archivio configurazione è disponibile per l'uso.</span><span class="sxs-lookup"><span data-stu-id="2992f-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="2992f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2992f-107">EXAMPLES</span></span>

### <span data-ttu-id="2992f-108">Esempio 1: verificare la disponibilità del nome dell'archivio di configurazione dell'app</span><span class="sxs-lookup"><span data-stu-id="2992f-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="2992f-109">Questo comando verifica la disponibilità del nome dell'archivio di configurazione dell'app.</span><span class="sxs-lookup"><span data-stu-id="2992f-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="2992f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2992f-110">PARAMETERS</span></span>

### <span data-ttu-id="2992f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2992f-111">-DefaultProfile</span></span>
<span data-ttu-id="2992f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2992f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2992f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2992f-113">-Name</span></span>
<span data-ttu-id="2992f-114">Il nome per verificare la disponibilità.</span><span class="sxs-lookup"><span data-stu-id="2992f-114">The name to check for availability.</span></span>

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

### <span data-ttu-id="2992f-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2992f-115">-SubscriptionId</span></span>
<span data-ttu-id="2992f-116">ID abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2992f-116">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="2992f-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2992f-117">-Confirm</span></span>
<span data-ttu-id="2992f-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2992f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2992f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2992f-119">-WhatIf</span></span>
<span data-ttu-id="2992f-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2992f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2992f-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2992f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2992f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2992f-122">CommonParameters</span></span>
<span data-ttu-id="2992f-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2992f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2992f-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2992f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2992f-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2992f-125">INPUTS</span></span>

## <span data-ttu-id="2992f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2992f-126">OUTPUTS</span></span>

### <span data-ttu-id="2992f-127">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="2992f-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="2992f-128">Note</span><span class="sxs-lookup"><span data-stu-id="2992f-128">NOTES</span></span>

<span data-ttu-id="2992f-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2992f-129">ALIASES</span></span>

## <span data-ttu-id="2992f-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2992f-130">RELATED LINKS</span></span>


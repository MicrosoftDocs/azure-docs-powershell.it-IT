---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 434f59a7b81449fe0e07b0324c1df6408da1ce81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978925"
---
# <span data-ttu-id="bc059-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="bc059-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="bc059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc059-102">SYNOPSIS</span></span>
<span data-ttu-id="bc059-103">Elenca la chiave di accesso per l'archivio di configurazione specificato.</span><span class="sxs-lookup"><span data-stu-id="bc059-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="bc059-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc059-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc059-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bc059-105">DESCRIPTION</span></span>
<span data-ttu-id="bc059-106">Elenca la chiave di accesso per l'archivio di configurazione specificato.</span><span class="sxs-lookup"><span data-stu-id="bc059-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="bc059-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc059-107">EXAMPLES</span></span>

### <span data-ttu-id="bc059-108">Esempio 1: Elencare tutte le chiavi dell'archivio di un archivio di configurazione delle app</span><span class="sxs-lookup"><span data-stu-id="bc059-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="bc059-109">Questo comando elenca tutte le chiavi dell'archivio di un archivio di configurazione delle app.</span><span class="sxs-lookup"><span data-stu-id="bc059-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="bc059-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc059-110">PARAMETERS</span></span>

### <span data-ttu-id="bc059-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc059-111">-DefaultProfile</span></span>
<span data-ttu-id="bc059-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc059-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc059-113">-Name</span><span class="sxs-lookup"><span data-stu-id="bc059-113">-Name</span></span>
<span data-ttu-id="bc059-114">Nome dell'archivio di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bc059-114">The name of the configuration store.</span></span>

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

### <span data-ttu-id="bc059-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc059-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc059-116">Nome del gruppo di risorse a cui appartiene il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bc059-116">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="bc059-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc059-117">-SubscriptionId</span></span>
<span data-ttu-id="bc059-118">ID sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bc059-118">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc059-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc059-119">-Confirm</span></span>
<span data-ttu-id="bc059-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc059-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc059-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc059-121">-WhatIf</span></span>
<span data-ttu-id="bc059-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc059-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc059-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc059-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc059-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc059-124">CommonParameters</span></span>
<span data-ttu-id="bc059-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc059-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc059-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc059-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc059-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="bc059-127">INPUTS</span></span>

## <span data-ttu-id="bc059-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc059-128">OUTPUTS</span></span>

### <span data-ttu-id="bc059-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="bc059-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="bc059-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="bc059-130">NOTES</span></span>

<span data-ttu-id="bc059-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="bc059-131">ALIASES</span></span>

## <span data-ttu-id="bc059-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc059-132">RELATED LINKS</span></span>


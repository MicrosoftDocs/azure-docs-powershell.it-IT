---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: 82e5f6ced22b17c8966afbd5bc57324ab2069d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991646"
---
# <span data-ttu-id="a3176-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="a3176-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="a3176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3176-102">SYNOPSIS</span></span>
<span data-ttu-id="a3176-103">Ottenere le chiavi di accesso della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a3176-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="a3176-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3176-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3176-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3176-105">DESCRIPTION</span></span>
<span data-ttu-id="a3176-106">Ottenere le chiavi di accesso della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a3176-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="a3176-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3176-107">EXAMPLES</span></span>

### <span data-ttu-id="a3176-108">Esempio 1: Recuperare la chiave per il servizio di comunicazione specificato</span><span class="sxs-lookup"><span data-stu-id="a3176-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="a3176-109">Visualizza la chiave e la stringa di connessione per il servizio di comunicazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a3176-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="a3176-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3176-110">PARAMETERS</span></span>

### <span data-ttu-id="a3176-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="a3176-111">-CommunicationServiceName</span></span>
<span data-ttu-id="a3176-112">Nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a3176-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="a3176-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3176-113">-DefaultProfile</span></span>
<span data-ttu-id="a3176-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3176-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3176-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3176-115">-ResourceGroupName</span></span>
<span data-ttu-id="a3176-116">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a3176-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a3176-117">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="a3176-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a3176-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3176-118">-SubscriptionId</span></span>
<span data-ttu-id="a3176-119">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a3176-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a3176-120">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a3176-120">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a3176-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3176-121">-Confirm</span></span>
<span data-ttu-id="a3176-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3176-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3176-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3176-123">-WhatIf</span></span>
<span data-ttu-id="a3176-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3176-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3176-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3176-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3176-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3176-126">CommonParameters</span></span>
<span data-ttu-id="a3176-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3176-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3176-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3176-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3176-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3176-129">INPUTS</span></span>

## <span data-ttu-id="a3176-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3176-130">OUTPUTS</span></span>

### <span data-ttu-id="a3176-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a3176-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="a3176-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3176-132">NOTES</span></span>

<span data-ttu-id="a3176-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a3176-133">ALIASES</span></span>

## <span data-ttu-id="a3176-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3176-134">RELATED LINKS</span></span>


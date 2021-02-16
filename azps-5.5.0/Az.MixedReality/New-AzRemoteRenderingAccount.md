---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180199"
---
# <span data-ttu-id="4c1d3-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="4c1d3-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="4c1d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1d3-103">Creare un account per il rendering remoto</span><span class="sxs-lookup"><span data-stu-id="4c1d3-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="4c1d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c1d3-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c1d3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c1d3-105">DESCRIPTION</span></span>
<span data-ttu-id="4c1d3-106">Creare un nuovo account per il rendering remoto in determinati tipi di sottoscrizione, gruppo di risorse e area geografica.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="4c1d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c1d3-107">EXAMPLES</span></span>

### <span data-ttu-id="4c1d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c1d3-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="4c1d3-109">Creare un nuovo account per il rendering remoto "esempio" nella sottoscrizione corrente, nel gruppo di risorse "rg1" e negli Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="4c1d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c1d3-110">PARAMETERS</span></span>

### <span data-ttu-id="4c1d3-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c1d3-111">-Confirm</span></span>
<span data-ttu-id="4c1d3-112">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c1d3-113">-DefaultProfile</span></span>
<span data-ttu-id="4c1d3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1d3-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4c1d3-115">-Location</span></span>
<span data-ttu-id="4c1d3-116">Posizione dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1d3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4c1d3-117">-Name</span></span>
<span data-ttu-id="4c1d3-118">Nome dell'account per il rendering remoto.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c1d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="4c1d3-120">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1d3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c1d3-121">-WhatIf</span></span>
<span data-ttu-id="4c1d3-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c1d3-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1d3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1d3-124">CommonParameters</span></span>
<span data-ttu-id="4c1d3-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c1d3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4c1d3-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c1d3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1d3-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c1d3-127">INPUTS</span></span>

### <span data-ttu-id="4c1d3-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4c1d3-128">None</span></span>

## <span data-ttu-id="4c1d3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c1d3-129">OUTPUTS</span></span>

### <span data-ttu-id="4c1d3-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="4c1d3-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="4c1d3-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c1d3-131">NOTES</span></span>

## <span data-ttu-id="4c1d3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c1d3-132">RELATED LINKS</span></span>

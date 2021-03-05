---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: d028e66fc5f1f4b2c3ab520bd76615e8e9e79099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982814"
---
# <span data-ttu-id="e9622-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="e9622-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="e9622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9622-102">SYNOPSIS</span></span>
<span data-ttu-id="e9622-103">Metodo per eseguire come account.</span><span class="sxs-lookup"><span data-stu-id="e9622-103">Method to get run as account.</span></span>

## <span data-ttu-id="e9622-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9622-104">SYNTAX</span></span>

### <span data-ttu-id="e9622-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9622-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e9622-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e9622-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e9622-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9622-107">DESCRIPTION</span></span>
<span data-ttu-id="e9622-108">Metodo per eseguire come account.</span><span class="sxs-lookup"><span data-stu-id="e9622-108">Method to get run as account.</span></span>

## <span data-ttu-id="e9622-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9622-109">EXAMPLES</span></span>

### <span data-ttu-id="e9622-110">Esempio 1: Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9622-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="e9622-111">Elencare tutti gli account eseguiti come account in un sito.</span><span class="sxs-lookup"><span data-stu-id="e9622-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="e9622-112">Esempio 2: Ottenere</span><span class="sxs-lookup"><span data-stu-id="e9622-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="e9622-113">Ottenere Esegui come account in base al nome.</span><span class="sxs-lookup"><span data-stu-id="e9622-113">Get Run as account by name.</span></span>

## <span data-ttu-id="e9622-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9622-114">PARAMETERS</span></span>

### <span data-ttu-id="e9622-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9622-115">-AccountName</span></span>
<span data-ttu-id="e9622-116">Eseguire come nome ARM account.</span><span class="sxs-lookup"><span data-stu-id="e9622-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9622-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9622-117">-DefaultProfile</span></span>
<span data-ttu-id="e9622-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9622-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9622-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9622-119">-ResourceGroupName</span></span>
<span data-ttu-id="e9622-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9622-120">The name of the resource group.</span></span>
<span data-ttu-id="e9622-121">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e9622-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e9622-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="e9622-122">-SiteName</span></span>
<span data-ttu-id="e9622-123">Nome del sito.</span><span class="sxs-lookup"><span data-stu-id="e9622-123">Site name.</span></span>

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

### <span data-ttu-id="e9622-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9622-124">-SubscriptionId</span></span>
<span data-ttu-id="e9622-125">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e9622-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e9622-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9622-126">CommonParameters</span></span>
<span data-ttu-id="e9622-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9622-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9622-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9622-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9622-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9622-129">INPUTS</span></span>

## <span data-ttu-id="e9622-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9622-130">OUTPUTS</span></span>

### <span data-ttu-id="e9622-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="e9622-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="e9622-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9622-132">NOTES</span></span>

<span data-ttu-id="e9622-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e9622-133">ALIASES</span></span>

## <span data-ttu-id="e9622-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9622-134">RELATED LINKS</span></span>


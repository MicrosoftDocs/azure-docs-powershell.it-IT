---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202339"
---
# <span data-ttu-id="36718-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="36718-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="36718-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36718-102">SYNOPSIS</span></span>
<span data-ttu-id="36718-103">Metodo per ottenere l'esecuzione come account.</span><span class="sxs-lookup"><span data-stu-id="36718-103">Method to get run as account.</span></span>

## <span data-ttu-id="36718-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36718-104">SYNTAX</span></span>

### <span data-ttu-id="36718-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36718-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36718-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="36718-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36718-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36718-107">DESCRIPTION</span></span>
<span data-ttu-id="36718-108">Metodo per ottenere l'esecuzione come account.</span><span class="sxs-lookup"><span data-stu-id="36718-108">Method to get run as account.</span></span>

## <span data-ttu-id="36718-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36718-109">EXAMPLES</span></span>

### <span data-ttu-id="36718-110">Esempio 1: elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36718-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="36718-111">Elenca tutti gli account RunAs in un sito.</span><span class="sxs-lookup"><span data-stu-id="36718-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="36718-112">Esempio 2: ottenere</span><span class="sxs-lookup"><span data-stu-id="36718-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="36718-113">Viene eseguito come account per nome.</span><span class="sxs-lookup"><span data-stu-id="36718-113">Get Run as account by name.</span></span>

## <span data-ttu-id="36718-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36718-114">PARAMETERS</span></span>

### <span data-ttu-id="36718-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36718-115">-AccountName</span></span>
<span data-ttu-id="36718-116">Esegui come nome del braccio dell'account.</span><span class="sxs-lookup"><span data-stu-id="36718-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="36718-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36718-117">-DefaultProfile</span></span>
<span data-ttu-id="36718-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36718-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36718-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36718-119">-ResourceGroupName</span></span>
<span data-ttu-id="36718-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36718-120">The name of the resource group.</span></span>
<span data-ttu-id="36718-121">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="36718-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36718-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="36718-122">-SiteName</span></span>
<span data-ttu-id="36718-123">Nome sito.</span><span class="sxs-lookup"><span data-stu-id="36718-123">Site name.</span></span>

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

### <span data-ttu-id="36718-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36718-124">-SubscriptionId</span></span>
<span data-ttu-id="36718-125">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="36718-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36718-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36718-126">CommonParameters</span></span>
<span data-ttu-id="36718-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36718-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36718-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36718-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36718-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36718-129">INPUTS</span></span>

## <span data-ttu-id="36718-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36718-130">OUTPUTS</span></span>

### <span data-ttu-id="36718-131">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api202001. IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="36718-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="36718-132">Note</span><span class="sxs-lookup"><span data-stu-id="36718-132">NOTES</span></span>

<span data-ttu-id="36718-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="36718-133">ALIASES</span></span>

## <span data-ttu-id="36718-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36718-134">RELATED LINKS</span></span>


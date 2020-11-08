---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202367"
---
# <span data-ttu-id="5c8f3-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="5c8f3-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="5c8f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8f3-103">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="5c8f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c8f3-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5c8f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="5c8f3-106">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="5c8f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c8f3-107">EXAMPLES</span></span>

### <span data-ttu-id="5c8f3-108">Esempio 1: elencare tutti i DB della replica in un MariaDB</span><span class="sxs-lookup"><span data-stu-id="5c8f3-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5c8f3-109">Questo comando elenca tutti i DB della replica in un MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="5c8f3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c8f3-110">PARAMETERS</span></span>

### <span data-ttu-id="5c8f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8f3-111">-DefaultProfile</span></span>
<span data-ttu-id="5c8f3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c8f3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c8f3-113">-ResourceGroupName</span></span>
<span data-ttu-id="5c8f3-114">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5c8f3-115">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5c8f3-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5c8f3-116">-ServerName</span></span>
<span data-ttu-id="5c8f3-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-117">The name of the server.</span></span>

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

### <span data-ttu-id="5c8f3-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c8f3-118">-SubscriptionId</span></span>
<span data-ttu-id="5c8f3-119">ID sottoscrizione che identifica un abbonamento a Azure.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5c8f3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8f3-120">CommonParameters</span></span>
<span data-ttu-id="5c8f3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8f3-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c8f3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8f3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c8f3-123">INPUTS</span></span>

## <span data-ttu-id="5c8f3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c8f3-124">OUTPUTS</span></span>

### <span data-ttu-id="5c8f3-125">Microsoft. Azure. PowerShell. Cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="5c8f3-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5c8f3-126">Note</span><span class="sxs-lookup"><span data-stu-id="5c8f3-126">NOTES</span></span>

<span data-ttu-id="5c8f3-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5c8f3-127">ALIASES</span></span>

## <span data-ttu-id="5c8f3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c8f3-128">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: c6fef537c3a0cc01bd2de01e00b69c1a69f81e3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970654"
---
# <span data-ttu-id="83bdc-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="83bdc-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="83bdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="83bdc-103">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="83bdc-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="83bdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83bdc-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="83bdc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="83bdc-106">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="83bdc-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="83bdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83bdc-107">EXAMPLES</span></span>

### <span data-ttu-id="83bdc-108">Esempio 1: Elencare tutti i database di replica in un database di MariaDB</span><span class="sxs-lookup"><span data-stu-id="83bdc-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="83bdc-109">Questo comando elenca tutti i database di replica in un database di MariaDB.</span><span class="sxs-lookup"><span data-stu-id="83bdc-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="83bdc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83bdc-110">PARAMETERS</span></span>

### <span data-ttu-id="83bdc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83bdc-111">-DefaultProfile</span></span>
<span data-ttu-id="83bdc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83bdc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83bdc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83bdc-113">-ResourceGroupName</span></span>
<span data-ttu-id="83bdc-114">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="83bdc-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="83bdc-115">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="83bdc-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="83bdc-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="83bdc-116">-ServerName</span></span>
<span data-ttu-id="83bdc-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="83bdc-117">The name of the server.</span></span>

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

### <span data-ttu-id="83bdc-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83bdc-118">-SubscriptionId</span></span>
<span data-ttu-id="83bdc-119">ID sottoscrizione che identifica una sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="83bdc-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="83bdc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83bdc-120">CommonParameters</span></span>
<span data-ttu-id="83bdc-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83bdc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83bdc-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83bdc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83bdc-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="83bdc-123">INPUTS</span></span>

## <span data-ttu-id="83bdc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83bdc-124">OUTPUTS</span></span>

### <span data-ttu-id="83bdc-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="83bdc-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="83bdc-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="83bdc-126">NOTES</span></span>

<span data-ttu-id="83bdc-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="83bdc-127">ALIASES</span></span>

## <span data-ttu-id="83bdc-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83bdc-128">RELATED LINKS</span></span>


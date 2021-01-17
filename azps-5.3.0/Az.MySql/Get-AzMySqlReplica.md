---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486831"
---
# <span data-ttu-id="3265f-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="3265f-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="3265f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3265f-102">SYNOPSIS</span></span>
<span data-ttu-id="3265f-103">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="3265f-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3265f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3265f-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3265f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3265f-105">DESCRIPTION</span></span>
<span data-ttu-id="3265f-106">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="3265f-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="3265f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3265f-107">EXAMPLES</span></span>

### <span data-ttu-id="3265f-108">Esempio 1: ottenere la replica del server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="3265f-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="3265f-109">Questo cmdlet ottiene la replica del server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="3265f-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="3265f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3265f-110">PARAMETERS</span></span>

### <span data-ttu-id="3265f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3265f-111">-DefaultProfile</span></span>
<span data-ttu-id="3265f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3265f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3265f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3265f-113">-ResourceGroupName</span></span>
<span data-ttu-id="3265f-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3265f-114">The name of the resource group.</span></span>
<span data-ttu-id="3265f-115">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="3265f-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3265f-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="3265f-116">-ServerName</span></span>
<span data-ttu-id="3265f-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="3265f-117">The name of the server.</span></span>

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

### <span data-ttu-id="3265f-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3265f-118">-SubscriptionId</span></span>
<span data-ttu-id="3265f-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3265f-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3265f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3265f-120">CommonParameters</span></span>
<span data-ttu-id="3265f-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3265f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3265f-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3265f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3265f-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3265f-123">INPUTS</span></span>

## <span data-ttu-id="3265f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3265f-124">OUTPUTS</span></span>

### <span data-ttu-id="3265f-125">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="3265f-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3265f-126">Note</span><span class="sxs-lookup"><span data-stu-id="3265f-126">NOTES</span></span>

<span data-ttu-id="3265f-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="3265f-127">ALIASES</span></span>

## <span data-ttu-id="3265f-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3265f-128">RELATED LINKS</span></span>


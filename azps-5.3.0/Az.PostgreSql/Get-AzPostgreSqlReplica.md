---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384520"
---
# <span data-ttu-id="41978-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="41978-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="41978-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41978-102">SYNOPSIS</span></span>
<span data-ttu-id="41978-103">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="41978-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="41978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41978-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="41978-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41978-105">DESCRIPTION</span></span>
<span data-ttu-id="41978-106">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="41978-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="41978-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41978-107">EXAMPLES</span></span>

### <span data-ttu-id="41978-108">Esempio 1: ottenere la replica del server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="41978-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="41978-109">Questo cmdlet ottiene la replica del server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="41978-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="41978-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41978-110">PARAMETERS</span></span>

### <span data-ttu-id="41978-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41978-111">-DefaultProfile</span></span>
<span data-ttu-id="41978-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41978-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41978-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41978-113">-ResourceGroupName</span></span>
<span data-ttu-id="41978-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41978-114">The name of the resource group.</span></span>
<span data-ttu-id="41978-115">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="41978-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="41978-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="41978-116">-ServerName</span></span>
<span data-ttu-id="41978-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="41978-117">The name of the server.</span></span>

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

### <span data-ttu-id="41978-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41978-118">-SubscriptionId</span></span>
<span data-ttu-id="41978-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="41978-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="41978-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41978-120">CommonParameters</span></span>
<span data-ttu-id="41978-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41978-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41978-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41978-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41978-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41978-123">INPUTS</span></span>

## <span data-ttu-id="41978-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41978-124">OUTPUTS</span></span>

### <span data-ttu-id="41978-125">Microsoft. Azure. PowerShell. Cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="41978-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="41978-126">Note</span><span class="sxs-lookup"><span data-stu-id="41978-126">NOTES</span></span>

<span data-ttu-id="41978-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="41978-127">ALIASES</span></span>

## <span data-ttu-id="41978-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41978-128">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179150"
---
# <span data-ttu-id="28902-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="28902-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="28902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28902-102">SYNOPSIS</span></span>
<span data-ttu-id="28902-103">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="28902-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="28902-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28902-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="28902-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="28902-105">DESCRIPTION</span></span>
<span data-ttu-id="28902-106">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="28902-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="28902-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28902-107">EXAMPLES</span></span>

### <span data-ttu-id="28902-108">Esempio 1: Ottenere la replica del server PostgreSql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="28902-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="28902-109">Questo cmdlet ottiene la replica del server PostgreSql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="28902-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="28902-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28902-110">PARAMETERS</span></span>

### <span data-ttu-id="28902-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28902-111">-DefaultProfile</span></span>
<span data-ttu-id="28902-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28902-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28902-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28902-113">-ResourceGroupName</span></span>
<span data-ttu-id="28902-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="28902-114">The name of the resource group.</span></span>
<span data-ttu-id="28902-115">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="28902-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="28902-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28902-116">-ServerName</span></span>
<span data-ttu-id="28902-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="28902-117">The name of the server.</span></span>

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

### <span data-ttu-id="28902-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28902-118">-SubscriptionId</span></span>
<span data-ttu-id="28902-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="28902-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="28902-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28902-120">CommonParameters</span></span>
<span data-ttu-id="28902-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28902-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28902-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28902-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28902-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="28902-123">INPUTS</span></span>

## <span data-ttu-id="28902-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28902-124">OUTPUTS</span></span>

### <span data-ttu-id="28902-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="28902-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="28902-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="28902-126">NOTES</span></span>

<span data-ttu-id="28902-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="28902-127">ALIASES</span></span>

## <span data-ttu-id="28902-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28902-128">RELATED LINKS</span></span>


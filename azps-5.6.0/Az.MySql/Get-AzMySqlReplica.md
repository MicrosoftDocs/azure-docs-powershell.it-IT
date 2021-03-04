---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: d4579ec17d870c1f002ce40309aa580226ff143d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962830"
---
# <span data-ttu-id="1dbad-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="1dbad-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="1dbad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbad-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbad-103">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="1dbad-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="1dbad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dbad-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1dbad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1dbad-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbad-106">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="1dbad-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="1dbad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dbad-107">EXAMPLES</span></span>

### <span data-ttu-id="1dbad-108">Esempio 1: Ottenere la replica del server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="1dbad-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="1dbad-109">Questo cmdlet recupera la replica del server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="1dbad-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="1dbad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbad-110">PARAMETERS</span></span>

### <span data-ttu-id="1dbad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbad-111">-DefaultProfile</span></span>
<span data-ttu-id="1dbad-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbad-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbad-113">-ResourceGroupName</span></span>
<span data-ttu-id="1dbad-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dbad-114">The name of the resource group.</span></span>
<span data-ttu-id="1dbad-115">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1dbad-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1dbad-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1dbad-116">-ServerName</span></span>
<span data-ttu-id="1dbad-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="1dbad-117">The name of the server.</span></span>

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

### <span data-ttu-id="1dbad-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1dbad-118">-SubscriptionId</span></span>
<span data-ttu-id="1dbad-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1dbad-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1dbad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbad-120">CommonParameters</span></span>
<span data-ttu-id="1dbad-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbad-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1dbad-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbad-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="1dbad-123">INPUTS</span></span>

## <span data-ttu-id="1dbad-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dbad-124">OUTPUTS</span></span>

### <span data-ttu-id="1dbad-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="1dbad-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="1dbad-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1dbad-126">NOTES</span></span>

<span data-ttu-id="1dbad-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1dbad-127">ALIASES</span></span>

## <span data-ttu-id="1dbad-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dbad-128">RELATED LINKS</span></span>


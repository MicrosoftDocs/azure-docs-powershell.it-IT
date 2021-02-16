---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180095"
---
# <span data-ttu-id="351b7-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="351b7-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="351b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="351b7-102">SYNOPSIS</span></span>
<span data-ttu-id="351b7-103">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="351b7-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="351b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="351b7-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="351b7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="351b7-105">DESCRIPTION</span></span>
<span data-ttu-id="351b7-106">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="351b7-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="351b7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="351b7-107">EXAMPLES</span></span>

### <span data-ttu-id="351b7-108">Esempio 1: Ottenere la replica del server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="351b7-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="351b7-109">Questo cmdlet recupera la replica del server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="351b7-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="351b7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="351b7-110">PARAMETERS</span></span>

### <span data-ttu-id="351b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351b7-111">-DefaultProfile</span></span>
<span data-ttu-id="351b7-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="351b7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="351b7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="351b7-113">-ResourceGroupName</span></span>
<span data-ttu-id="351b7-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="351b7-114">The name of the resource group.</span></span>
<span data-ttu-id="351b7-115">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="351b7-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="351b7-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="351b7-116">-ServerName</span></span>
<span data-ttu-id="351b7-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="351b7-117">The name of the server.</span></span>

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

### <span data-ttu-id="351b7-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="351b7-118">-SubscriptionId</span></span>
<span data-ttu-id="351b7-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="351b7-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="351b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351b7-120">CommonParameters</span></span>
<span data-ttu-id="351b7-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="351b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351b7-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="351b7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351b7-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="351b7-123">INPUTS</span></span>

## <span data-ttu-id="351b7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="351b7-124">OUTPUTS</span></span>

### <span data-ttu-id="351b7-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="351b7-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="351b7-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="351b7-126">NOTES</span></span>

<span data-ttu-id="351b7-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="351b7-127">ALIASES</span></span>

## <span data-ttu-id="351b7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="351b7-128">RELATED LINKS</span></span>


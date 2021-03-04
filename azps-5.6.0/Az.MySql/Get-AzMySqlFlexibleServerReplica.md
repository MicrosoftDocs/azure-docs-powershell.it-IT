---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 25444df39945527d1bc574283e397407e0218633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962845"
---
# <span data-ttu-id="f9a34-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="f9a34-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="f9a34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9a34-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a34-103">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="f9a34-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="f9a34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9a34-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f9a34-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9a34-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a34-106">Elencare tutte le replica per un determinato server.</span><span class="sxs-lookup"><span data-stu-id="f9a34-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="f9a34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9a34-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a34-108">Esempio 1: Ottenere la replica del server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="f9a34-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="f9a34-109">Questo cmdlet recupera la replica del server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="f9a34-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="f9a34-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9a34-110">PARAMETERS</span></span>

### <span data-ttu-id="f9a34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a34-111">-DefaultProfile</span></span>
<span data-ttu-id="f9a34-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a34-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9a34-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9a34-113">-ResourceGroupName</span></span>
<span data-ttu-id="f9a34-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9a34-114">The name of the resource group.</span></span>
<span data-ttu-id="f9a34-115">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f9a34-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f9a34-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f9a34-116">-ServerName</span></span>
<span data-ttu-id="f9a34-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="f9a34-117">The name of the server.</span></span>

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

### <span data-ttu-id="f9a34-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9a34-118">-SubscriptionId</span></span>
<span data-ttu-id="f9a34-119">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f9a34-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f9a34-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a34-120">CommonParameters</span></span>
<span data-ttu-id="f9a34-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a34-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a34-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9a34-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a34-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9a34-123">INPUTS</span></span>

## <span data-ttu-id="f9a34-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9a34-124">OUTPUTS</span></span>

### <span data-ttu-id="f9a34-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="f9a34-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="f9a34-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9a34-126">NOTES</span></span>

<span data-ttu-id="f9a34-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f9a34-127">ALIASES</span></span>

## <span data-ttu-id="f9a34-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9a34-128">RELATED LINKS</span></span>


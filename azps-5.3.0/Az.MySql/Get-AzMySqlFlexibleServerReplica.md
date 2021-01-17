---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486832"
---
# <span data-ttu-id="4a95e-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="4a95e-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="4a95e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a95e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a95e-103">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="4a95e-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4a95e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a95e-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4a95e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a95e-105">DESCRIPTION</span></span>
<span data-ttu-id="4a95e-106">Elencare tutte le repliche per un server specifico.</span><span class="sxs-lookup"><span data-stu-id="4a95e-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4a95e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a95e-107">EXAMPLES</span></span>

### <span data-ttu-id="4a95e-108">Esempio 1: ottenere la replica del server MySql in base al gruppo di risorse e al nome del server</span><span class="sxs-lookup"><span data-stu-id="4a95e-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="4a95e-109">Questo cmdlet ottiene la replica del server MySql in base al gruppo di risorse e al nome del server.</span><span class="sxs-lookup"><span data-stu-id="4a95e-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="4a95e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a95e-110">PARAMETERS</span></span>

### <span data-ttu-id="4a95e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a95e-111">-DefaultProfile</span></span>
<span data-ttu-id="4a95e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a95e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a95e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a95e-113">-ResourceGroupName</span></span>
<span data-ttu-id="4a95e-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a95e-114">The name of the resource group.</span></span>
<span data-ttu-id="4a95e-115">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="4a95e-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4a95e-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4a95e-116">-ServerName</span></span>
<span data-ttu-id="4a95e-117">Nome del server.</span><span class="sxs-lookup"><span data-stu-id="4a95e-117">The name of the server.</span></span>

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

### <span data-ttu-id="4a95e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a95e-118">-SubscriptionId</span></span>
<span data-ttu-id="4a95e-119">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4a95e-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4a95e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a95e-120">CommonParameters</span></span>
<span data-ttu-id="4a95e-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a95e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a95e-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a95e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a95e-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a95e-123">INPUTS</span></span>

## <span data-ttu-id="4a95e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a95e-124">OUTPUTS</span></span>

### <span data-ttu-id="4a95e-125">Microsoft. Azure. PowerShell. Cmdlets. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="4a95e-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="4a95e-126">Note</span><span class="sxs-lookup"><span data-stu-id="4a95e-126">NOTES</span></span>

<span data-ttu-id="4a95e-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4a95e-127">ALIASES</span></span>

## <span data-ttu-id="4a95e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a95e-128">RELATED LINKS</span></span>


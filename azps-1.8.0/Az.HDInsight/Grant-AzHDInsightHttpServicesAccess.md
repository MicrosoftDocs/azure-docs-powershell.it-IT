---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: c531135af3d118a9987a3c328eb4c06847e75fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836027"
---
# <span data-ttu-id="124e5-101">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="124e5-101">Grant-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="124e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="124e5-102">SYNOPSIS</span></span>
<span data-ttu-id="124e5-103">Concede l'accesso HTTP al cluster.</span><span class="sxs-lookup"><span data-stu-id="124e5-103">Grants HTTP access to the cluster.</span></span>

## <span data-ttu-id="124e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="124e5-104">SYNTAX</span></span>

```
Grant-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="124e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="124e5-105">DESCRIPTION</span></span>
<span data-ttu-id="124e5-106">Il cmdlet **Grant-AzHDInsightHttpServicesAccess** concede l'accesso HTTP a un cluster HDInsight di Azure tramite ODBC, Ambari, oozie e servizi Web.</span><span class="sxs-lookup"><span data-stu-id="124e5-106">The **Grant-AzHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="124e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="124e5-107">EXAMPLES</span></span>

### <span data-ttu-id="124e5-108">Esempio 1: concedere l'accesso HTTP a un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="124e5-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="124e5-109">Questo comando concede l'accesso HTTP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="124e5-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="124e5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="124e5-110">PARAMETERS</span></span>

### <span data-ttu-id="124e5-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="124e5-111">-ClusterName</span></span>
<span data-ttu-id="124e5-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="124e5-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="124e5-113">-DefaultProfile</span></span>
<span data-ttu-id="124e5-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="124e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e5-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="124e5-115">-HttpCredential</span></span>
<span data-ttu-id="124e5-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="124e5-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="124e5-117">-ResourceGroupName</span></span>
<span data-ttu-id="124e5-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="124e5-118">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="124e5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="124e5-119">CommonParameters</span></span>
<span data-ttu-id="124e5-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="124e5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="124e5-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="124e5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="124e5-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="124e5-122">INPUTS</span></span>

### <span data-ttu-id="124e5-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="124e5-123">None</span></span>

## <span data-ttu-id="124e5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="124e5-124">OUTPUTS</span></span>

### <span data-ttu-id="124e5-125">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="124e5-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="124e5-126">Note</span><span class="sxs-lookup"><span data-stu-id="124e5-126">NOTES</span></span>

## <span data-ttu-id="124e5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="124e5-127">RELATED LINKS</span></span>

[<span data-ttu-id="124e5-128">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="124e5-128">Revoke-AzHDInsightHttpServicesAccess</span></span>](./Revoke-AzHDInsightHttpServicesAccess.md)



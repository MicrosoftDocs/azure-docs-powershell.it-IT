---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: c447d8dbfb7ed0b1fb4cf2ac3ad4c63aa4666ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688309"
---
# <span data-ttu-id="19173-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="19173-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="19173-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19173-102">SYNOPSIS</span></span>
<span data-ttu-id="19173-103">Concede l'accesso HTTP al cluster.</span><span class="sxs-lookup"><span data-stu-id="19173-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19173-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19173-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19173-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19173-105">DESCRIPTION</span></span>
<span data-ttu-id="19173-106">Il cmdlet **Grant-AzureRmHDInsightHttpServicesAccess** concede l'accesso HTTP a un cluster HDInsight di Azure tramite ODBC, Ambari, oozie e servizi Web.</span><span class="sxs-lookup"><span data-stu-id="19173-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="19173-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19173-107">EXAMPLES</span></span>

### <span data-ttu-id="19173-108">Esempio 1: concedere l'accesso HTTP a un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="19173-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="19173-109">Questo comando concede l'accesso HTTP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="19173-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="19173-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19173-110">PARAMETERS</span></span>

### <span data-ttu-id="19173-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="19173-111">-ClusterName</span></span>
<span data-ttu-id="19173-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="19173-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="19173-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="19173-113">-HttpCredential</span></span>
<span data-ttu-id="19173-114">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="19173-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="19173-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19173-115">-ResourceGroupName</span></span>
<span data-ttu-id="19173-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="19173-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="19173-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19173-117">-DefaultProfile</span></span>
<span data-ttu-id="19173-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19173-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19173-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19173-119">CommonParameters</span></span>
<span data-ttu-id="19173-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19173-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19173-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19173-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19173-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19173-122">INPUTS</span></span>

## <span data-ttu-id="19173-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19173-123">OUTPUTS</span></span>

### <span data-ttu-id="19173-124">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="19173-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="19173-125">Note</span><span class="sxs-lookup"><span data-stu-id="19173-125">NOTES</span></span>

## <span data-ttu-id="19173-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19173-126">RELATED LINKS</span></span>

[<span data-ttu-id="19173-127">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="19173-127">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)



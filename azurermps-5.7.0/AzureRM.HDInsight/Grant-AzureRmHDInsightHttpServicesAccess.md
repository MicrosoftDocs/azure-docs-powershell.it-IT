---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 529eedf9cd8ae782d08af7d349d4e11885a8a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511175"
---
# <span data-ttu-id="0d109-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0d109-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="0d109-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d109-102">SYNOPSIS</span></span>
<span data-ttu-id="0d109-103">Concede l'accesso HTTP al cluster.</span><span class="sxs-lookup"><span data-stu-id="0d109-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d109-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d109-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d109-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d109-105">DESCRIPTION</span></span>
<span data-ttu-id="0d109-106">Il cmdlet **Grant-AzureRmHDInsightHttpServicesAccess** concede l'accesso HTTP a un cluster HDInsight di Azure tramite ODBC, Ambari, oozie e servizi Web.</span><span class="sxs-lookup"><span data-stu-id="0d109-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="0d109-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d109-107">EXAMPLES</span></span>

### <span data-ttu-id="0d109-108">Esempio 1: concedere l'accesso HTTP a un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="0d109-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="0d109-109">Questo comando concede l'accesso HTTP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="0d109-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0d109-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d109-110">PARAMETERS</span></span>

### <span data-ttu-id="0d109-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0d109-111">-ClusterName</span></span>
<span data-ttu-id="0d109-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0d109-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d109-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d109-113">-DefaultProfile</span></span>
<span data-ttu-id="0d109-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0d109-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d109-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="0d109-115">-HttpCredential</span></span>
<span data-ttu-id="0d109-116">Specifica le credenziali di accesso al cluster (HTTP) per il cluster.</span><span class="sxs-lookup"><span data-stu-id="0d109-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d109-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d109-117">-ResourceGroupName</span></span>
<span data-ttu-id="0d109-118">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d109-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d109-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d109-119">CommonParameters</span></span>
<span data-ttu-id="0d109-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d109-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d109-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d109-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d109-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d109-122">INPUTS</span></span>

### <span data-ttu-id="0d109-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0d109-123">None</span></span>
<span data-ttu-id="0d109-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0d109-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d109-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d109-125">OUTPUTS</span></span>

### <span data-ttu-id="0d109-126">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="0d109-126">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="0d109-127">Note</span><span class="sxs-lookup"><span data-stu-id="0d109-127">NOTES</span></span>

## <span data-ttu-id="0d109-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d109-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d109-129">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0d109-129">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)



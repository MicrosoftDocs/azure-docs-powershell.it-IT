---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 388e339ba7545bc2e4d00166a6f365a19cb44f28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518999"
---
# <span data-ttu-id="8eb95-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8eb95-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="8eb95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8eb95-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb95-103">Disabilita l'accesso HTTP al cluster.</span><span class="sxs-lookup"><span data-stu-id="8eb95-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eb95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8eb95-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eb95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8eb95-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb95-106">Il cmdlet **Revoke-AzureRmHDInsightHttpServicesAccess** Disabilita l'accesso HTTP a un cluster HDInsight di Azure per ODBC, Ambari, oozie e webHCatalog Web Services.</span><span class="sxs-lookup"><span data-stu-id="8eb95-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="8eb95-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8eb95-107">EXAMPLES</span></span>

### <span data-ttu-id="8eb95-108">Esempio 1: disabilitare l'accesso HTTP a un cluster</span><span class="sxs-lookup"><span data-stu-id="8eb95-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="8eb95-109">Questo comando revoca l'accesso HTTP al cluster denominato your-hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="8eb95-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="8eb95-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8eb95-110">PARAMETERS</span></span>

### <span data-ttu-id="8eb95-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="8eb95-111">-ClusterName</span></span>
<span data-ttu-id="8eb95-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="8eb95-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8eb95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb95-113">-DefaultProfile</span></span>
<span data-ttu-id="8eb95-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8eb95-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8eb95-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb95-115">-ResourceGroupName</span></span>
<span data-ttu-id="8eb95-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8eb95-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8eb95-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb95-117">CommonParameters</span></span>
<span data-ttu-id="8eb95-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb95-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb95-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb95-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb95-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8eb95-120">INPUTS</span></span>

### <span data-ttu-id="8eb95-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8eb95-121">None</span></span>
<span data-ttu-id="8eb95-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8eb95-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8eb95-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8eb95-123">OUTPUTS</span></span>

### <span data-ttu-id="8eb95-124">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="8eb95-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="8eb95-125">Note</span><span class="sxs-lookup"><span data-stu-id="8eb95-125">NOTES</span></span>

## <span data-ttu-id="8eb95-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8eb95-126">RELATED LINKS</span></span>

[<span data-ttu-id="8eb95-127">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="8eb95-127">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)



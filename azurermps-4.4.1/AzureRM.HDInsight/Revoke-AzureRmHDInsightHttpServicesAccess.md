---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 795882aa421037252ca920093f1df39b4e242fce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510608"
---
# <span data-ttu-id="cbd61-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cbd61-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="cbd61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbd61-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd61-103">Disabilita l'accesso HTTP al cluster.</span><span class="sxs-lookup"><span data-stu-id="cbd61-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbd61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbd61-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbd61-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbd61-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd61-106">Il cmdlet **Revoke-AzureRmHDInsightHttpServicesAccess** Disabilita l'accesso HTTP a un cluster HDInsight di Azure per ODBC, Ambari, oozie e webHCatalog Web Services.</span><span class="sxs-lookup"><span data-stu-id="cbd61-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="cbd61-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbd61-107">EXAMPLES</span></span>

### <span data-ttu-id="cbd61-108">Esempio 1: disabilitare l'accesso HTTP a un cluster</span><span class="sxs-lookup"><span data-stu-id="cbd61-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="cbd61-109">Questo comando revoca l'accesso HTTP al cluster denominato your-hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="cbd61-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="cbd61-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbd61-110">PARAMETERS</span></span>

### <span data-ttu-id="cbd61-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="cbd61-111">-ClusterName</span></span>
<span data-ttu-id="cbd61-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="cbd61-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cbd61-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd61-113">-ResourceGroupName</span></span>
<span data-ttu-id="cbd61-114">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cbd61-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cbd61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd61-115">-DefaultProfile</span></span>
<span data-ttu-id="cbd61-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd61-117">CommonParameters</span></span>
<span data-ttu-id="cbd61-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd61-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd61-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd61-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbd61-120">INPUTS</span></span>

## <span data-ttu-id="cbd61-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbd61-121">OUTPUTS</span></span>

### <span data-ttu-id="cbd61-122">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="cbd61-122">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="cbd61-123">Note</span><span class="sxs-lookup"><span data-stu-id="cbd61-123">NOTES</span></span>

## <span data-ttu-id="cbd61-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbd61-124">RELATED LINKS</span></span>

[<span data-ttu-id="cbd61-125">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cbd61-125">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)



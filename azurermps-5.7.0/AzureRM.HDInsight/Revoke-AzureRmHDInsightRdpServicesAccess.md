---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 32664beb1ffe7600756953294b1ec33f7d1d54ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519464"
---
# <span data-ttu-id="96515-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="96515-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="96515-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96515-102">SYNOPSIS</span></span>
<span data-ttu-id="96515-103">Disabilita l'accesso RDP a un cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="96515-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96515-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96515-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96515-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96515-105">DESCRIPTION</span></span>
<span data-ttu-id="96515-106">Il cmdlet **Revoke-AzureRmHDInsightRdpServicesAccess** Disabilita l'accesso RDP (Remote Desktop Protocol) a un cluster HDInsight di Azure basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="96515-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="96515-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96515-107">EXAMPLES</span></span>

### <span data-ttu-id="96515-108">Esempio 1: disabilitare l'accesso RDP a un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="96515-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="96515-109">Questo comando revoca l'accesso RDP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="96515-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="96515-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96515-110">PARAMETERS</span></span>

### <span data-ttu-id="96515-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="96515-111">-ClusterName</span></span>
<span data-ttu-id="96515-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="96515-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="96515-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96515-113">-DefaultProfile</span></span>
<span data-ttu-id="96515-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="96515-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96515-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96515-115">-ResourceGroupName</span></span>
<span data-ttu-id="96515-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96515-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="96515-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96515-117">CommonParameters</span></span>
<span data-ttu-id="96515-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96515-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96515-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96515-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96515-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96515-120">INPUTS</span></span>

### <span data-ttu-id="96515-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="96515-121">None</span></span>
<span data-ttu-id="96515-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="96515-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96515-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96515-123">OUTPUTS</span></span>

### <span data-ttu-id="96515-124">System. void</span><span class="sxs-lookup"><span data-stu-id="96515-124">System.Void</span></span>

## <span data-ttu-id="96515-125">Note</span><span class="sxs-lookup"><span data-stu-id="96515-125">NOTES</span></span>

## <span data-ttu-id="96515-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96515-126">RELATED LINKS</span></span>

[<span data-ttu-id="96515-127">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="96515-127">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)



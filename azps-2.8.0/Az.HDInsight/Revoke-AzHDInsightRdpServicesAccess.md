---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674290"
---
# <span data-ttu-id="c94ad-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c94ad-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="c94ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c94ad-102">SYNOPSIS</span></span>
<span data-ttu-id="c94ad-103">Disabilita l'accesso RDP a un cluster Windows.</span><span class="sxs-lookup"><span data-stu-id="c94ad-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="c94ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c94ad-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c94ad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c94ad-105">DESCRIPTION</span></span>
<span data-ttu-id="c94ad-106">Il cmdlet **Revoke-AzHDInsightRdpServicesAccess** Disabilita l'accesso RDP (Remote Desktop Protocol) a un cluster HDInsight di Azure basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="c94ad-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="c94ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c94ad-107">EXAMPLES</span></span>

### <span data-ttu-id="c94ad-108">Esempio 1: disabilitare l'accesso RDP a un cluster specificato</span><span class="sxs-lookup"><span data-stu-id="c94ad-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="c94ad-109">Questo comando revoca l'accesso RDP al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="c94ad-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c94ad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c94ad-110">PARAMETERS</span></span>

### <span data-ttu-id="c94ad-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c94ad-111">-ClusterName</span></span>
<span data-ttu-id="c94ad-112">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c94ad-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c94ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c94ad-113">-DefaultProfile</span></span>
<span data-ttu-id="c94ad-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c94ad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c94ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c94ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="c94ad-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c94ad-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c94ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c94ad-117">CommonParameters</span></span>
<span data-ttu-id="c94ad-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c94ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c94ad-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c94ad-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c94ad-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c94ad-120">INPUTS</span></span>

### <span data-ttu-id="c94ad-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c94ad-121">None</span></span>

## <span data-ttu-id="c94ad-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c94ad-122">OUTPUTS</span></span>

### <span data-ttu-id="c94ad-123">System. void</span><span class="sxs-lookup"><span data-stu-id="c94ad-123">System.Void</span></span>

## <span data-ttu-id="c94ad-124">Note</span><span class="sxs-lookup"><span data-stu-id="c94ad-124">NOTES</span></span>

## <span data-ttu-id="c94ad-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c94ad-125">RELATED LINKS</span></span>

[<span data-ttu-id="c94ad-126">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="c94ad-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)



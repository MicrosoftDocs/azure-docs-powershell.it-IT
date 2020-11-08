---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023678"
---
# <span data-ttu-id="8c518-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="8c518-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="8c518-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c518-102">SYNOPSIS</span></span>
<span data-ttu-id="8c518-103">Aggiunge un'azione di script HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8c518-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="8c518-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c518-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c518-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c518-105">DESCRIPTION</span></span>
<span data-ttu-id="8c518-106">Questa versione di Azure PowerShell HDInsight è deprecata.</span><span class="sxs-lookup"><span data-stu-id="8c518-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="8c518-107">Questi cmdlet verranno rimossi dal 1 ° gennaio 2017.</span><span class="sxs-lookup"><span data-stu-id="8c518-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="8c518-108">Usare la versione più recente di Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8c518-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="8c518-109">Per informazioni su come usare il nuovo HDInsight per creare un cluster, vedere [creare cluster basati su Linux in HDInsight con Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="8c518-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="8c518-110">Per informazioni su come inviare processi con Azure PowerShell e altri approcci, vedere [inviare processi di Hadoop in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="8c518-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="8c518-111">Per informazioni di riferimento su Azure PowerShell HDInsight, vedere [cmdlet di Azure HDInsight](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8c518-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="8c518-112">Il cmdlet **Add-AzureHDInsightScriptAction** fornisce le funzionalità di Azure HDInsight usate per installare software aggiuntivo o per modificare la configurazione delle applicazioni eseguite in un cluster di Hadoop usando gli script di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c518-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="8c518-113">Un'azione di script viene eseguita sui nodi del cluster quando vengono distribuiti i cluster di HDInsight e vengono eseguiti dopo i nodi della configurazione completa di HDInsight del cluster.</span><span class="sxs-lookup"><span data-stu-id="8c518-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="8c518-114">L'azione script viene eseguita in privilegi di amministratore di sistema e fornisce i diritti di accesso completo ai nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="8c518-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="8c518-115">Puoi specificare ogni cluster con un elenco di azioni di script da eseguire in una sequenza specificata.</span><span class="sxs-lookup"><span data-stu-id="8c518-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="8c518-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c518-116">EXAMPLES</span></span>

### <span data-ttu-id="8c518-117">Esempio 1: aggiungere un'azione di script a un cluster</span><span class="sxs-lookup"><span data-stu-id="8c518-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="8c518-118">Il primo comando usa il cmdlet **New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight e quindi lo archivia nella variabile $config.</span><span class="sxs-lookup"><span data-stu-id="8c518-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="8c518-119">Il secondo comando usa il cmdlet **Add-AzureHDInsightScriptAction** per aggiungere l'azione script denominata TestScriptAction a $config.</span><span class="sxs-lookup"><span data-stu-id="8c518-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="8c518-120">Il comando finale usa il cmdlet **New-AzureHDInsightCluster** per creare un nuovo cluster di HDInsight che esegue l'azione di script archiviata in $config.</span><span class="sxs-lookup"><span data-stu-id="8c518-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="8c518-121">Esempio 2: aggiungere più azioni di script a un cluster</span><span class="sxs-lookup"><span data-stu-id="8c518-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="8c518-122">Il primo comando usa il cmdlet **New-AzureHDInsightClusterConfig** per creare una configurazione di cluster HDInsight e quindi lo archivia nella variabile $config.</span><span class="sxs-lookup"><span data-stu-id="8c518-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="8c518-123">Il secondo comando usa il cmdlet **Add-AzureHDInsightScriptAction** per aggiungere l'azione di script specificata a $config e quindi usa l'operatore pipeline per passare una seconda volta $config a **Add-AzureHDInsightScriptAction** per aggiungere una seconda azione di script a $config.</span><span class="sxs-lookup"><span data-stu-id="8c518-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="8c518-124">Il comando finale usa il cmdlet **New-AzureHDInsightCluster** per creare un cluster che esegue le azioni di script in $config.</span><span class="sxs-lookup"><span data-stu-id="8c518-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="8c518-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c518-125">PARAMETERS</span></span>

### <span data-ttu-id="8c518-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="8c518-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="8c518-127">Specifica i nodi per cui eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="8c518-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="8c518-128">I valori accettabili per questo parametro sono: HeadNode o dataNode.</span><span class="sxs-lookup"><span data-stu-id="8c518-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="8c518-129">Puoi specificare un valore o entrambi i valori.</span><span class="sxs-lookup"><span data-stu-id="8c518-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c518-130">-Config</span><span class="sxs-lookup"><span data-stu-id="8c518-130">-Config</span></span>
<span data-ttu-id="8c518-131">Specifica un oggetto Configuration.</span><span class="sxs-lookup"><span data-stu-id="8c518-131">Specifies a configuration object.</span></span>
<span data-ttu-id="8c518-132">Questo cmdlet aggiunge informazioni sulle azioni di script all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="8c518-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c518-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c518-133">-Name</span></span>
<span data-ttu-id="8c518-134">Specifica il nome di un'azione di script.</span><span class="sxs-lookup"><span data-stu-id="8c518-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c518-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="8c518-135">-Parameters</span></span>
<span data-ttu-id="8c518-136">Specifica i parametri necessari per un'azione di script.</span><span class="sxs-lookup"><span data-stu-id="8c518-136">Specifies the parameters that are required by a script action.</span></span>

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

### <span data-ttu-id="8c518-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="8c518-137">-Profile</span></span>
<span data-ttu-id="8c518-138">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c518-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c518-139">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="8c518-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c518-140">-URI</span><span class="sxs-lookup"><span data-stu-id="8c518-140">-Uri</span></span>
<span data-ttu-id="8c518-141">Specifica la posizione URI di uno script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="8c518-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c518-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c518-142">CommonParameters</span></span>
<span data-ttu-id="8c518-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c518-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c518-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c518-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c518-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c518-145">INPUTS</span></span>

## <span data-ttu-id="8c518-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c518-146">OUTPUTS</span></span>

## <span data-ttu-id="8c518-147">Note</span><span class="sxs-lookup"><span data-stu-id="8c518-147">NOTES</span></span>

## <span data-ttu-id="8c518-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c518-148">RELATED LINKS</span></span>

[<span data-ttu-id="8c518-149">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8c518-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="8c518-150">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="8c518-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)



---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178263"
---
# <span data-ttu-id="3acd2-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="3acd2-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="3acd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3acd2-102">SYNOPSIS</span></span>
<span data-ttu-id="3acd2-103">Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="3acd2-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="3acd2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3acd2-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="3acd2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3acd2-105">DESCRIPTION</span></span>
<span data-ttu-id="3acd2-106">Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure Stack HCI.</span><span class="sxs-lookup"><span data-stu-id="3acd2-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="3acd2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3acd2-107">EXAMPLES</span></span>

### <span data-ttu-id="3acd2-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="3acd2-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
<span data-ttu-id="3acd2-109">Richiamo in uno dei nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="3acd2-109">Invoking on one of the cluster node.</span></span> <span data-ttu-id="3acd2-110">Caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3acd2-110">Success case.</span></span>

### <span data-ttu-id="3acd2-111">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="3acd2-111">EXAMPLE 2</span></span>
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
<span data-ttu-id="3acd2-112">Richiamo in uno dei nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="3acd2-112">Invoking on one of the cluster node.</span></span> <span data-ttu-id="3acd2-113">Caso non riuscito.</span><span class="sxs-lookup"><span data-stu-id="3acd2-113">Failed case.</span></span>

## <span data-ttu-id="3acd2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3acd2-114">PARAMETERS</span></span>

### <span data-ttu-id="3acd2-115">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="3acd2-115">-ComputerName</span></span>
<span data-ttu-id="3acd2-116">Specifica uno del nodo del cluster nel cluster locale che viene registrato in Azure.</span><span class="sxs-lookup"><span data-stu-id="3acd2-116">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3acd2-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="3acd2-117">-Credential</span></span>
<span data-ttu-id="3acd2-118">Specifica le credenziali per NomeComputer.</span><span class="sxs-lookup"><span data-stu-id="3acd2-118">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="3acd2-119">Il valore predefinito è l'utente corrente che esegue il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3acd2-119">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3acd2-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="3acd2-120">-EnvironmentName</span></span>
<span data-ttu-id="3acd2-121">Specifica l'ambiente di Azure.</span><span class="sxs-lookup"><span data-stu-id="3acd2-121">Specifies the Azure Environment.</span></span>
<span data-ttu-id="3acd2-122">Il valore predefinito è AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="3acd2-122">Default is AzureCloud.</span></span>
<span data-ttu-id="3acd2-123">I valori validi sono AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="3acd2-123">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3acd2-124">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="3acd2-124">-Region</span></span>
<span data-ttu-id="3acd2-125">Specifica l'area geografica a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="3acd2-125">Specifies the Region to connect to.</span></span>
<span data-ttu-id="3acd2-126">Non usato a meno che non si tratta dell'area Canary.</span><span class="sxs-lookup"><span data-stu-id="3acd2-126">Not used unless it is Canary region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3acd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3acd2-127">CommonParameters</span></span>
<span data-ttu-id="3acd2-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3acd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3acd2-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3acd2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3acd2-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="3acd2-130">INPUTS</span></span>

## <span data-ttu-id="3acd2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3acd2-131">OUTPUTS</span></span>

### <span data-ttu-id="3acd2-132">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="3acd2-132">PSCustomObject.</span></span> <span data-ttu-id="3acd2-133">Restituisce le proprietà seguenti in PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="3acd2-133">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="3acd2-134">Test: nome del test eseguito.</span><span class="sxs-lookup"><span data-stu-id="3acd2-134">Test: Name of the test performed.</span></span>
### <span data-ttu-id="3acd2-135">EndpointTested: endpoint utilizzato nel test.</span><span class="sxs-lookup"><span data-stu-id="3acd2-135">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="3acd2-136">IsRequired: True o False</span><span class="sxs-lookup"><span data-stu-id="3acd2-136">IsRequired: True or False</span></span>
### <span data-ttu-id="3acd2-137">Risultato: Operazione riuscita o Non riuscita</span><span class="sxs-lookup"><span data-stu-id="3acd2-137">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="3acd2-138">FailedNodes: elenco dei nodi in cui il test non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3acd2-138">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="3acd2-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="3acd2-139">NOTES</span></span>

## <span data-ttu-id="3acd2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3acd2-140">RELATED LINKS</span></span>

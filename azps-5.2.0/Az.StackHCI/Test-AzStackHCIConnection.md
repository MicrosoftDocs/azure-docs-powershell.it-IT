---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 1183a2aa6bf452d77ebe3975024067244075e5fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349924"
---
# <span data-ttu-id="46e6c-101">Test-AzStackHCIConnection</span><span class="sxs-lookup"><span data-stu-id="46e6c-101">Test-AzStackHCIConnection</span></span>

## <span data-ttu-id="46e6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="46e6c-103">Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure stack HCI.</span><span class="sxs-lookup"><span data-stu-id="46e6c-103">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="46e6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46e6c-104">SYNTAX</span></span>

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="46e6c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="46e6c-106">Test-AzStackHCIConnection verifica la connettività dai nodi cluster locali ai servizi di Azure richiesti da Azure stack HCI.</span><span class="sxs-lookup"><span data-stu-id="46e6c-106">Test-AzStackHCIConnection verifies connectivity from on-premises clustered nodes to the Azure services required by Azure Stack HCI.</span></span>

## <span data-ttu-id="46e6c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="46e6c-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="46e6c-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node. Success case.
```

<span data-ttu-id="46e6c-109">Test C:\PS \> -test di AzStackHCIConnection: connettersi al servizio EndpointTested di Azure stack HCI: https://azurestackhci-df.azurefd.net/health richiesto: risultato effettivo: riuscito</span><span class="sxs-lookup"><span data-stu-id="46e6c-109">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Succeeded</span></span>

### <span data-ttu-id="46e6c-110">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="46e6c-110">EXAMPLE 2</span></span>
```
Invoking on one of the cluster node. Failed case.
```

<span data-ttu-id="46e6c-111">Test C:\PS \> -test di AzStackHCIConnection: connettersi al servizio di Azure stack HCI EndpointTested: https://azurestackhci-df.azurefd.net/health richiesto: risultato effettivo: errore FailedNodes: Node1inClus2, Node2inClus3</span><span class="sxs-lookup"><span data-stu-id="46e6c-111">C:\PS\>Test-AzStackHCIConnection Test: Connect to Azure Stack HCI Service EndpointTested: https://azurestackhci-df.azurefd.net/health IsRequired: True Result: Failed FailedNodes: Node1inClus2, Node2inClus3</span></span>

## <span data-ttu-id="46e6c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46e6c-112">PARAMETERS</span></span>

### <span data-ttu-id="46e6c-113">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="46e6c-113">-ComputerName</span></span>
<span data-ttu-id="46e6c-114">Specifica uno dei nodi del cluster nel cluster locale che viene registrato in Azure.</span><span class="sxs-lookup"><span data-stu-id="46e6c-114">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="46e6c-115">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="46e6c-115">-Credential</span></span>
<span data-ttu-id="46e6c-116">Specifica le credenziali per nomecomputer.</span><span class="sxs-lookup"><span data-stu-id="46e6c-116">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="46e6c-117">Il valore predefinito è l'esecuzione del cmdlet da parte dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="46e6c-117">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="46e6c-118">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="46e6c-118">-EnvironmentName</span></span>
<span data-ttu-id="46e6c-119">Specifica l'ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="46e6c-119">Specifies the Azure Environment.</span></span>
<span data-ttu-id="46e6c-120">Il valore predefinito è AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="46e6c-120">Default is AzureCloud.</span></span>
<span data-ttu-id="46e6c-121">I valori validi sono AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="46e6c-121">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="46e6c-122">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="46e6c-122">-Region</span></span>
<span data-ttu-id="46e6c-123">Specifica l'area geografica a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="46e6c-123">Specifies the Region to connect to.</span></span>
<span data-ttu-id="46e6c-124">Non usato a meno che non sia l'area Canarie.</span><span class="sxs-lookup"><span data-stu-id="46e6c-124">Not used unless it is Canary region.</span></span>

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

### <span data-ttu-id="46e6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e6c-125">CommonParameters</span></span>
<span data-ttu-id="46e6c-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e6c-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46e6c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e6c-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46e6c-128">INPUTS</span></span>

## <span data-ttu-id="46e6c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46e6c-129">OUTPUTS</span></span>

### <span data-ttu-id="46e6c-130">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="46e6c-130">PSCustomObject.</span></span> <span data-ttu-id="46e6c-131">Restituisce le proprietà seguenti in PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="46e6c-131">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="46e6c-132">Test: nome del test eseguito.</span><span class="sxs-lookup"><span data-stu-id="46e6c-132">Test: Name of the test performed.</span></span>
### <span data-ttu-id="46e6c-133">EndpointTested: endpoint usato nel test.</span><span class="sxs-lookup"><span data-stu-id="46e6c-133">EndpointTested: Endpoint used in the test.</span></span>
### <span data-ttu-id="46e6c-134">Obbligatorio: vero o falso</span><span class="sxs-lookup"><span data-stu-id="46e6c-134">IsRequired: True or False</span></span>
### <span data-ttu-id="46e6c-135">Risultato: riuscito o non riuscito</span><span class="sxs-lookup"><span data-stu-id="46e6c-135">Result: Succeeded or Failed</span></span>
### <span data-ttu-id="46e6c-136">FailedNodes: elenco dei nodi in cui il test non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="46e6c-136">FailedNodes: List of nodes on which the test failed.</span></span>
## <span data-ttu-id="46e6c-137">Note</span><span class="sxs-lookup"><span data-stu-id="46e6c-137">NOTES</span></span>

## <span data-ttu-id="46e6c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46e6c-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: e29ee3c51b94964db286a999630196b46ad9f786
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854553"
---
# <span data-ttu-id="da335-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="da335-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="da335-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da335-102">SYNOPSIS</span></span>
<span data-ttu-id="da335-103">Rimuovere un certificato cluster da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="da335-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="da335-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da335-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da335-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da335-105">DESCRIPTION</span></span>
<span data-ttu-id="da335-106">Usare **Remove-AzServiceFabricClusterCertificate** per rimuovere un certificato cluster dal cluster, purché esista un altro certificato valido già in uso nel cluster.</span><span class="sxs-lookup"><span data-stu-id="da335-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="da335-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da335-107">EXAMPLES</span></span>

### <span data-ttu-id="da335-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da335-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="da335-109">Questo comando rimuove il certificato con 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A di identificazione personale da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="da335-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="da335-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da335-110">PARAMETERS</span></span>

### <span data-ttu-id="da335-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da335-111">-DefaultProfile</span></span>
<span data-ttu-id="da335-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da335-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da335-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="da335-113">-Name</span></span>
<span data-ttu-id="da335-114">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="da335-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da335-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da335-115">-ResourceGroupName</span></span>
<span data-ttu-id="da335-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da335-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da335-117">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="da335-117">-Thumbprint</span></span>
<span data-ttu-id="da335-118">Specificare l'identificazione personale del cluster da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="da335-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da335-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da335-119">-Confirm</span></span>
<span data-ttu-id="da335-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da335-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da335-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da335-121">-WhatIf</span></span>
<span data-ttu-id="da335-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da335-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da335-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da335-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da335-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da335-124">CommonParameters</span></span>
<span data-ttu-id="da335-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da335-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da335-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da335-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da335-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da335-127">INPUTS</span></span>

### <span data-ttu-id="da335-128">System. String</span><span class="sxs-lookup"><span data-stu-id="da335-128">System.String</span></span>

## <span data-ttu-id="da335-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da335-129">OUTPUTS</span></span>

### <span data-ttu-id="da335-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="da335-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="da335-131">Note</span><span class="sxs-lookup"><span data-stu-id="da335-131">NOTES</span></span>

## <span data-ttu-id="da335-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da335-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 088f90af1ce80bdda390de1ce62a9d38581344aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514796"
---
# <span data-ttu-id="3dc8e-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="3dc8e-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="3dc8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dc8e-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc8e-103">Rimuovere un certificato cluster da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dc8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dc8e-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dc8e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dc8e-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc8e-106">Usare **Remove-AzureRmServiceFabricClusterCertificate** per rimuovere un certificato cluster dal cluster, purché esista un altro certificato valido già in uso nel cluster.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="3dc8e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dc8e-107">EXAMPLES</span></span>

### <span data-ttu-id="3dc8e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3dc8e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="3dc8e-109">Questo comando rimuove il certificato con 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A di identificazione personale da usare per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="3dc8e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dc8e-110">PARAMETERS</span></span>

### <span data-ttu-id="3dc8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc8e-111">-DefaultProfile</span></span>
<span data-ttu-id="3dc8e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc8e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dc8e-113">-Name</span></span>
<span data-ttu-id="3dc8e-114">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="3dc8e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc8e-115">-ResourceGroupName</span></span>
<span data-ttu-id="3dc8e-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3dc8e-117">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="3dc8e-117">-Thumbprint</span></span>
<span data-ttu-id="3dc8e-118">Specificare l'identificazione personale del cluster da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="3dc8e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3dc8e-119">-Confirm</span></span>
<span data-ttu-id="3dc8e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc8e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc8e-121">-WhatIf</span></span>
<span data-ttu-id="3dc8e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dc8e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc8e-124">CommonParameters</span></span>
<span data-ttu-id="3dc8e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc8e-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc8e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc8e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dc8e-127">INPUTS</span></span>

### <span data-ttu-id="3dc8e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3dc8e-128">System.String</span></span>
<span data-ttu-id="3dc8e-129">Parametri: identificazione personale (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3dc8e-129">Parameters: Thumbprint (ByValue)</span></span>

## <span data-ttu-id="3dc8e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dc8e-130">OUTPUTS</span></span>

### <span data-ttu-id="3dc8e-131">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="3dc8e-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="3dc8e-132">Note</span><span class="sxs-lookup"><span data-stu-id="3dc8e-132">NOTES</span></span>

## <span data-ttu-id="3dc8e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dc8e-133">RELATED LINKS</span></span>

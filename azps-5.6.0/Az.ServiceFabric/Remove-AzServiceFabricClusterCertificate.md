---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 59f8723470707a644e426bd9559a8e982f731e6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005518"
---
# <span data-ttu-id="f8e49-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f8e49-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="f8e49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e49-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e49-103">Rimuovere un certificato cluster da usare per la sicurezza dei cluster.</span><span class="sxs-lookup"><span data-stu-id="f8e49-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="f8e49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8e49-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8e49-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f8e49-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e49-106">Usare **Remove-AzServiceFabricClusterCertificate** per rimuovere un certificato cluster dal cluster, purché nel cluster sia già in uso un altro certificato valido.</span><span class="sxs-lookup"><span data-stu-id="f8e49-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="f8e49-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8e49-107">EXAMPLES</span></span>

### <span data-ttu-id="f8e49-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8e49-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="f8e49-109">Questo comando rimuove il certificato con immagine thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A dall'uso per la sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="f8e49-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="f8e49-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8e49-110">PARAMETERS</span></span>

### <span data-ttu-id="f8e49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e49-111">-DefaultProfile</span></span>
<span data-ttu-id="f8e49-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e49-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f8e49-113">-Name</span></span>
<span data-ttu-id="f8e49-114">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="f8e49-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f8e49-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e49-115">-ResourceGroupName</span></span>
<span data-ttu-id="f8e49-116">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8e49-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f8e49-117">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="f8e49-117">-Thumbprint</span></span>
<span data-ttu-id="f8e49-118">Specificare l'impronta digitale del cluster da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f8e49-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="f8e49-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8e49-119">-Confirm</span></span>
<span data-ttu-id="f8e49-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8e49-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8e49-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8e49-121">-WhatIf</span></span>
<span data-ttu-id="f8e49-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8e49-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8e49-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8e49-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8e49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e49-124">CommonParameters</span></span>
<span data-ttu-id="f8e49-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8e49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e49-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8e49-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e49-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="f8e49-127">INPUTS</span></span>

### <span data-ttu-id="f8e49-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f8e49-128">System.String</span></span>

## <span data-ttu-id="f8e49-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8e49-129">OUTPUTS</span></span>

### <span data-ttu-id="f8e49-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f8e49-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f8e49-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="f8e49-131">NOTES</span></span>

## <span data-ttu-id="f8e49-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8e49-132">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020698"
---
# <span data-ttu-id="d93be-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="d93be-101">Get-AzAttestation</span></span>

## <span data-ttu-id="d93be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d93be-102">SYNOPSIS</span></span>
<span data-ttu-id="d93be-103">Ottiene un attestato.</span><span class="sxs-lookup"><span data-stu-id="d93be-103">Gets an attestation.</span></span>

## <span data-ttu-id="d93be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d93be-104">SYNTAX</span></span>

### <span data-ttu-id="d93be-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d93be-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d93be-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d93be-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d93be-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d93be-107">DESCRIPTION</span></span>
<span data-ttu-id="d93be-108">Il cmdlet Get-AzAttestation ottiene informazioni sull'attestazione in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d93be-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="d93be-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d93be-109">EXAMPLES</span></span>

### <span data-ttu-id="d93be-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d93be-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="d93be-111">Ottenere il provider di attestazioni *pshtest* nel gruppo di risorse *PSH-test-RG*.</span><span class="sxs-lookup"><span data-stu-id="d93be-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="d93be-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d93be-112">PARAMETERS</span></span>

### <span data-ttu-id="d93be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93be-113">-DefaultProfile</span></span>
<span data-ttu-id="d93be-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d93be-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d93be-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d93be-115">-Name</span></span>
<span data-ttu-id="d93be-116">Nome dell'attestazione.</span><span class="sxs-lookup"><span data-stu-id="d93be-116">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93be-117">-ResourceGroupName</span></span>
<span data-ttu-id="d93be-118">Specifica il nome del gruppo di risorse associato all'attestazione in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="d93be-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d93be-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d93be-119">-ResourceId</span></span>
<span data-ttu-id="d93be-120">Specifica il nome del ResourceID associato all'attestazione in cui viene eseguita la query</span><span class="sxs-lookup"><span data-stu-id="d93be-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d93be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93be-121">CommonParameters</span></span>
<span data-ttu-id="d93be-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d93be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93be-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d93be-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93be-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d93be-124">INPUTS</span></span>

### <span data-ttu-id="d93be-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d93be-125">System.String</span></span>

## <span data-ttu-id="d93be-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d93be-126">OUTPUTS</span></span>

### <span data-ttu-id="d93be-127">Microsoft. Azure. Commands. Attestation. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="d93be-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="d93be-128">Note</span><span class="sxs-lookup"><span data-stu-id="d93be-128">NOTES</span></span>

## <span data-ttu-id="d93be-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d93be-129">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675842"
---
# <span data-ttu-id="1cb79-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="1cb79-101">Get-AzAttestation</span></span>

## <span data-ttu-id="1cb79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1cb79-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb79-103">Ottiene un attestato.</span><span class="sxs-lookup"><span data-stu-id="1cb79-103">Gets an attestation.</span></span>

## <span data-ttu-id="1cb79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cb79-104">SYNTAX</span></span>

### <span data-ttu-id="1cb79-105">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1cb79-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1cb79-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb79-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cb79-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cb79-107">DESCRIPTION</span></span>
<span data-ttu-id="1cb79-108">Il cmdlet Get-AzAttestation ottiene informazioni sull'attestazione in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1cb79-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="1cb79-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cb79-109">EXAMPLES</span></span>

### <span data-ttu-id="1cb79-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1cb79-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="1cb79-111">Ottenere l'attestazione "esempio" nel gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="1cb79-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="1cb79-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1cb79-112">PARAMETERS</span></span>

### <span data-ttu-id="1cb79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb79-113">-DefaultProfile</span></span>
<span data-ttu-id="1cb79-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb79-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cb79-115">-Name</span></span>
<span data-ttu-id="1cb79-116">Nome dell'attestazione.</span><span class="sxs-lookup"><span data-stu-id="1cb79-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb79-117">-ResourceGroupName</span></span>
<span data-ttu-id="1cb79-118">Specifica il nome del gruppo di risorse associato all'attestazione in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="1cb79-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb79-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb79-119">-ResourceId</span></span>
<span data-ttu-id="1cb79-120">Specifica il nome del ResourceID associato all'attestazione in cui viene eseguita la query</span><span class="sxs-lookup"><span data-stu-id="1cb79-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb79-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb79-121">CommonParameters</span></span>
<span data-ttu-id="1cb79-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb79-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb79-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cb79-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb79-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1cb79-124">INPUTS</span></span>

### <span data-ttu-id="1cb79-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb79-125">System.String</span></span>

## <span data-ttu-id="1cb79-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cb79-126">OUTPUTS</span></span>

### <span data-ttu-id="1cb79-127">Microsoft. Azure. Commands. Attestation. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="1cb79-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="1cb79-128">Note</span><span class="sxs-lookup"><span data-stu-id="1cb79-128">NOTES</span></span>

## <span data-ttu-id="1cb79-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cb79-129">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: caf516dafc710b7b4884e33a4e2cc51b464581be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675512"
---
# <span data-ttu-id="1c1e0-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="1c1e0-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="1c1e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1e0-103">Ottiene le chiavi dell'API per un account.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="1c1e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c1e0-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c1e0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="1c1e0-106">Il cmdlet **Get-AzCognitiveServicesAccountKey** ottiene le chiavi API per un account di servizi cognitivi con provisioning.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="1c1e0-107">Un account di servizi cognitivi dispone di due chiavi API: key1 e key2.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="1c1e0-108">I tasti consentono l'interazione con l'endpoint dell'account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="1c1e0-109">Usare New-AzCognitiveServicesAccountKey per rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="1c1e0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c1e0-110">EXAMPLES</span></span>

### <span data-ttu-id="1c1e0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c1e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="1c1e0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c1e0-112">PARAMETERS</span></span>

### <span data-ttu-id="1c1e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1e0-113">-DefaultProfile</span></span>
<span data-ttu-id="1c1e0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1c1e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c1e0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c1e0-115">-Name</span></span>
<span data-ttu-id="1c1e0-116">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-116">Specifies the name of the account.</span></span>
<span data-ttu-id="1c1e0-117">Questo cmdlet ottiene le chiavi per l'account.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c1e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="1c1e0-119">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="1c1e0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1e0-120">CommonParameters</span></span>
<span data-ttu-id="1c1e0-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c1e0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1e0-122">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c1e0-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1e0-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c1e0-123">INPUTS</span></span>

### <span data-ttu-id="1c1e0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1c1e0-124">System.String</span></span>

## <span data-ttu-id="1c1e0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c1e0-125">OUTPUTS</span></span>

### <span data-ttu-id="1c1e0-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="1c1e0-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="1c1e0-127">Note</span><span class="sxs-lookup"><span data-stu-id="1c1e0-127">NOTES</span></span>

## <span data-ttu-id="1c1e0-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c1e0-128">RELATED LINKS</span></span>

[<span data-ttu-id="1c1e0-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="1c1e0-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: d4523dc240c015f4dea29b86e1285a9fce9afbc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673877"
---
# <span data-ttu-id="96969-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="96969-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="96969-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96969-102">SYNOPSIS</span></span>
<span data-ttu-id="96969-103">Ottiene le chiavi dell'API per un account.</span><span class="sxs-lookup"><span data-stu-id="96969-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="96969-104">Queste chiavi sono il meccanismo di autenticazione usato nelle successive chiamate ad Azure maps.</span><span class="sxs-lookup"><span data-stu-id="96969-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="96969-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96969-105">SYNTAX</span></span>

### <span data-ttu-id="96969-106">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96969-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96969-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96969-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96969-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96969-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96969-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96969-109">DESCRIPTION</span></span>
<span data-ttu-id="96969-110">Il cmdlet Get-AzMapsAccountKey ottiene le chiavi API per un account di mappe di Azure con provisioning.</span><span class="sxs-lookup"><span data-stu-id="96969-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="96969-111">Un account di Azure Maps include due chiavi API: primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="96969-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="96969-112">I tasti consentono l'interazione con l'endpoint dell'account di Azure maps.</span><span class="sxs-lookup"><span data-stu-id="96969-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="96969-113">USA New-AzMapsAccountKey (New-AzMapsAccountKey. MD) per rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="96969-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="96969-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96969-114">EXAMPLES</span></span>

### <span data-ttu-id="96969-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96969-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="96969-116">Restituisce le chiavi per l'account denominato nome account nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="96969-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="96969-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="96969-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="96969-118">Restituisce le chiavi dell'account Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="96969-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="96969-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96969-119">PARAMETERS</span></span>

### <span data-ttu-id="96969-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96969-120">-DefaultProfile</span></span>
<span data-ttu-id="96969-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96969-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96969-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96969-122">-InputObject</span></span>
<span data-ttu-id="96969-123">L'account di Maps viene inviato tramite pipe da Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="96969-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="96969-124">-Name</span></span>
<span data-ttu-id="96969-125">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="96969-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96969-126">-ResourceGroupName</span></span>
<span data-ttu-id="96969-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96969-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96969-128">-ResourceId</span></span>
<span data-ttu-id="96969-129">Mappe dell'account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="96969-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="96969-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96969-130">CommonParameters</span></span>
<span data-ttu-id="96969-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96969-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96969-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96969-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96969-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96969-133">INPUTS</span></span>

### <span data-ttu-id="96969-134">System. String</span><span class="sxs-lookup"><span data-stu-id="96969-134">System.String</span></span>

### <span data-ttu-id="96969-135">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="96969-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="96969-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96969-136">OUTPUTS</span></span>

### <span data-ttu-id="96969-137">Microsoft. Azure. Commands. maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="96969-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="96969-138">Note</span><span class="sxs-lookup"><span data-stu-id="96969-138">NOTES</span></span>

## <span data-ttu-id="96969-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96969-139">RELATED LINKS</span></span>

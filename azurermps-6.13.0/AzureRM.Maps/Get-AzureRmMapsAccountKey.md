---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccountKey.md
ms.openlocfilehash: 1afe0f8f93bd00a384e1bb741ed8ea54e1ae66d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516511"
---
# <span data-ttu-id="7e410-101">Get-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="7e410-101">Get-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="7e410-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e410-102">SYNOPSIS</span></span>
<span data-ttu-id="7e410-103">Ottiene le chiavi dell'API per un account.</span><span class="sxs-lookup"><span data-stu-id="7e410-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="7e410-104">Queste chiavi sono il meccanismo di autenticazione usato nelle successive chiamate ad Azure maps.</span><span class="sxs-lookup"><span data-stu-id="7e410-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e410-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e410-105">SYNTAX</span></span>

### <span data-ttu-id="7e410-106">NameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7e410-106">NameParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e410-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e410-107">InputObjectParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7e410-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e410-108">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e410-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e410-109">DESCRIPTION</span></span>
<span data-ttu-id="7e410-110">Il cmdlet Get-AzureRmMapsAccountKey ottiene le chiavi API per un account di mappe di Azure con provisioning.</span><span class="sxs-lookup"><span data-stu-id="7e410-110">The Get-AzureRmMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="7e410-111">Un account di Azure Maps include due chiavi API: primaria e secondaria.</span><span class="sxs-lookup"><span data-stu-id="7e410-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="7e410-112">I tasti consentono l'interazione con l'endpoint dell'account di Azure maps.</span><span class="sxs-lookup"><span data-stu-id="7e410-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="7e410-113">USA New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey. MD) per rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="7e410-113">Use New-AzureRmMapsAccountKey (New-AzureRmMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="7e410-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e410-114">EXAMPLES</span></span>

### <span data-ttu-id="7e410-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7e410-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7e410-116">Restituisce le chiavi per l'account denominato nome account nel gruppo di risorse MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7e410-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7e410-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7e410-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="7e410-118">Restituisce le chiavi dell'account Azure Maps specificato.</span><span class="sxs-lookup"><span data-stu-id="7e410-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="7e410-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e410-119">PARAMETERS</span></span>

### <span data-ttu-id="7e410-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e410-120">-DefaultProfile</span></span>
<span data-ttu-id="7e410-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e410-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e410-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e410-122">-InputObject</span></span>
<span data-ttu-id="7e410-123">L'account di Maps viene inviato tramite pipe da Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="7e410-123">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="7e410-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e410-124">-Name</span></span>
<span data-ttu-id="7e410-125">Nome dell'account mappe.</span><span class="sxs-lookup"><span data-stu-id="7e410-125">Maps Account Name.</span></span>

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

### <span data-ttu-id="7e410-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e410-126">-ResourceGroupName</span></span>
<span data-ttu-id="7e410-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e410-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e410-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e410-128">-ResourceId</span></span>
<span data-ttu-id="7e410-129">Mappe dell'account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7e410-129">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="7e410-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e410-130">CommonParameters</span></span>
<span data-ttu-id="7e410-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e410-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e410-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e410-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e410-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e410-133">INPUTS</span></span>

### <span data-ttu-id="7e410-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7e410-134">System.String</span></span>

### <span data-ttu-id="7e410-135">Microsoft. Azure. Commands. maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="7e410-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="7e410-136">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7e410-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7e410-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e410-137">OUTPUTS</span></span>

### <span data-ttu-id="7e410-138">Microsoft. Azure. Commands. maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7e410-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="7e410-139">Note</span><span class="sxs-lookup"><span data-stu-id="7e410-139">NOTES</span></span>

## <span data-ttu-id="7e410-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e410-140">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521143"
---
# <span data-ttu-id="d0e08-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0e08-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="d0e08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0e08-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e08-103">Filtra le entità del servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0e08-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0e08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0e08-104">SYNTAX</span></span>

### <span data-ttu-id="d0e08-105">EmptyParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0e08-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0e08-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e08-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0e08-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e08-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0e08-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e08-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0e08-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0e08-109">DESCRIPTION</span></span>
<span data-ttu-id="d0e08-110">Filtra le entità del servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0e08-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="d0e08-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0e08-111">EXAMPLES</span></span>

### <span data-ttu-id="d0e08-112">--------------------------Filtra le entità di servizio tramite SPN--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0e08-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="d0e08-113">Ottiene le entità di servizio con SPN 36f81fc3-b00f-48CD-8218-3879f51ff39f.</span><span class="sxs-lookup"><span data-stu-id="d0e08-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="d0e08-114">--------------------------Filtra le entità di servizio tramite la stringa di ricerca--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0e08-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="d0e08-115">Filtra tutte le entità del servizio Active Directory con nome visualizzato che iniziano con "Web".</span><span class="sxs-lookup"><span data-stu-id="d0e08-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="d0e08-116">--------------------------Elenco delle entità dei servizi pubblicitari--------------------------</span><span class="sxs-lookup"><span data-stu-id="d0e08-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="d0e08-117">Ottiene tutte le entità del servizio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0e08-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="d0e08-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0e08-118">PARAMETERS</span></span>

### <span data-ttu-id="d0e08-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d0e08-119">-ObjectId</span></span>
<span data-ttu-id="d0e08-120">ID oggetto dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d0e08-120">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e08-121">-SearchString</span><span class="sxs-lookup"><span data-stu-id="d0e08-121">-SearchString</span></span>
<span data-ttu-id="d0e08-122">Recupera tutte le entità di servizio che hanno il nome visualizzato a partire da questo valore.</span><span class="sxs-lookup"><span data-stu-id="d0e08-122">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e08-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d0e08-123">-ServicePrincipalName</span></span>
<span data-ttu-id="d0e08-124">SPN del servizio.</span><span class="sxs-lookup"><span data-stu-id="d0e08-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e08-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e08-125">-DefaultProfile</span></span>
<span data-ttu-id="d0e08-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e08-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e08-127">CommonParameters</span></span>
<span data-ttu-id="d0e08-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e08-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e08-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e08-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0e08-130">INPUTS</span></span>

## <span data-ttu-id="d0e08-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0e08-131">OUTPUTS</span></span>

### <span data-ttu-id="d0e08-132">System. Collections. Generic. list ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="d0e08-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="d0e08-133">Note</span><span class="sxs-lookup"><span data-stu-id="d0e08-133">NOTES</span></span>

## <span data-ttu-id="d0e08-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0e08-134">RELATED LINKS</span></span>

[<span data-ttu-id="d0e08-135">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0e08-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d0e08-136">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0e08-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d0e08-137">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d0e08-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="d0e08-138">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="d0e08-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="d0e08-139">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d0e08-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)


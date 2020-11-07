---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: a0f4c41b310e820b939500b8496b411d7b0266d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866451"
---
# <span data-ttu-id="7d30a-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7d30a-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="7d30a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d30a-102">SYNOPSIS</span></span>
<span data-ttu-id="7d30a-103">Recupera un elenco di credenziali associate a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="7d30a-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d30a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d30a-104">SYNTAX</span></span>

### <span data-ttu-id="7d30a-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d30a-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d30a-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d30a-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d30a-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d30a-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d30a-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d30a-108">SPNObjectParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d30a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d30a-109">DESCRIPTION</span></span>
<span data-ttu-id="7d30a-110">Il cmdlet Get-AzureRmADSpCredential può essere usato per recuperare un elenco di credenziali associate a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="7d30a-110">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="7d30a-111">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="7d30a-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="7d30a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d30a-112">EXAMPLES</span></span>

### <span data-ttu-id="7d30a-113">Esempio 1-credenziali elenco per SPN</span><span class="sxs-lookup"><span data-stu-id="7d30a-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="7d30a-114">Restituisce un elenco di credenziali associate all'entità servizio con SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="7d30a-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="7d30a-115">Esempio 2-credenziali elenco per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="7d30a-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="7d30a-116">Restituisce un elenco di credenziali associate all'entità servizio con l'ID oggetto "58e28616-99cc-4DA4-B705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="7d30a-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="7d30a-117">Esempio 3-credenziali elenco per piping</span><span class="sxs-lookup"><span data-stu-id="7d30a-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

<span data-ttu-id="7d30a-118">Ottiene l'entità servizio con l'ID oggetto "58e28616-99cc-4DA4-B705-7672130e1047" e lo convoglia al cmdlet Get-AzureRmADSpCredential per elencare tutte le credenziali per tale entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="7d30a-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzureRmADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="7d30a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d30a-119">PARAMETERS</span></span>

### <span data-ttu-id="7d30a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d30a-120">-DefaultProfile</span></span>
<span data-ttu-id="7d30a-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7d30a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d30a-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d30a-122">-DisplayName</span></span>
<span data-ttu-id="7d30a-123">Nome visualizzato dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="7d30a-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d30a-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7d30a-124">-ObjectId</span></span>
<span data-ttu-id="7d30a-125">ID oggetto dell'entità servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="7d30a-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d30a-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7d30a-126">-ServicePrincipalName</span></span>
<span data-ttu-id="7d30a-127">Nome (SPN) dell'entità servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="7d30a-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d30a-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="7d30a-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="7d30a-129">Oggetto Principal del servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="7d30a-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d30a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d30a-130">CommonParameters</span></span>
<span data-ttu-id="7d30a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d30a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d30a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d30a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d30a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d30a-133">INPUTS</span></span>

### <span data-ttu-id="7d30a-134">System. Guid</span><span class="sxs-lookup"><span data-stu-id="7d30a-134">System.Guid</span></span>

### <span data-ttu-id="7d30a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7d30a-135">System.String</span></span>

### <span data-ttu-id="7d30a-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7d30a-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="7d30a-137">Parametri: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d30a-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="7d30a-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d30a-138">OUTPUTS</span></span>

### <span data-ttu-id="7d30a-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="7d30a-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="7d30a-140">Note</span><span class="sxs-lookup"><span data-stu-id="7d30a-140">NOTES</span></span>

## <span data-ttu-id="7d30a-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d30a-141">RELATED LINKS</span></span>

[<span data-ttu-id="7d30a-142">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7d30a-142">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="7d30a-143">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7d30a-143">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="7d30a-144">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7d30a-144">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


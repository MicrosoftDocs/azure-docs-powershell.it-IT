---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188946"
---
# <span data-ttu-id="13852-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="13852-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="13852-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="13852-102">SYNOPSIS</span></span>
<span data-ttu-id="13852-103">Recupera un elenco di credenziali associate a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="13852-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="13852-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13852-104">SYNTAX</span></span>

### <span data-ttu-id="13852-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13852-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13852-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="13852-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13852-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="13852-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13852-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13852-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13852-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13852-109">DESCRIPTION</span></span>
<span data-ttu-id="13852-110">Il cmdlet Get-AzADSpCredential può essere usato per recuperare un elenco di credenziali associate a un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="13852-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="13852-111">Questo comando consente di recuperare tutte le proprietà delle credenziali, ma non il valore delle credenziali, associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="13852-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="13852-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13852-112">EXAMPLES</span></span>

### <span data-ttu-id="13852-113">Esempio 1-credenziali elenco per SPN</span><span class="sxs-lookup"><span data-stu-id="13852-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="13852-114">Restituisce un elenco di credenziali associate all'entità servizio con SPN ' http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="13852-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="13852-115">Esempio 2-credenziali elenco per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="13852-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="13852-116">Restituisce un elenco di credenziali associate all'entità servizio con l'ID oggetto "58e28616-99cc-4DA4-B705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="13852-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="13852-117">Esempio 3-credenziali elenco per piping</span><span class="sxs-lookup"><span data-stu-id="13852-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="13852-118">Ottiene l'entità servizio con l'ID oggetto "58e28616-99cc-4DA4-B705-7672130e1047" e lo convoglia al cmdlet Get-AzADSpCredential per elencare tutte le credenziali per tale entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="13852-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="13852-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="13852-119">PARAMETERS</span></span>

### <span data-ttu-id="13852-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13852-120">-DefaultProfile</span></span>
<span data-ttu-id="13852-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="13852-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13852-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="13852-122">-DisplayName</span></span>
<span data-ttu-id="13852-123">Nome visualizzato dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="13852-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="13852-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="13852-124">-ObjectId</span></span>
<span data-ttu-id="13852-125">ID oggetto dell'entità servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="13852-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13852-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="13852-126">-ServicePrincipalName</span></span>
<span data-ttu-id="13852-127">Nome (SPN) dell'entità servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="13852-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="13852-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="13852-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="13852-129">Oggetto Principal del servizio per il recupero delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="13852-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13852-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13852-130">CommonParameters</span></span>
<span data-ttu-id="13852-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13852-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13852-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13852-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13852-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="13852-133">INPUTS</span></span>

### <span data-ttu-id="13852-134">System. String</span><span class="sxs-lookup"><span data-stu-id="13852-134">System.String</span></span>

### <span data-ttu-id="13852-135">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="13852-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="13852-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13852-136">OUTPUTS</span></span>

### <span data-ttu-id="13852-137">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="13852-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="13852-138">Note</span><span class="sxs-lookup"><span data-stu-id="13852-138">NOTES</span></span>

## <span data-ttu-id="13852-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13852-139">RELATED LINKS</span></span>

[<span data-ttu-id="13852-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="13852-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="13852-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="13852-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="13852-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="13852-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

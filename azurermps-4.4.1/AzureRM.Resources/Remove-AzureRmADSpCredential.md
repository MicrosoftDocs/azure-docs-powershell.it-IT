---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: b1f4b8d53a1031cef76d51a87bbf9afa5b75758f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687709"
---
# <span data-ttu-id="ceee9-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ceee9-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="ceee9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ceee9-102">SYNOPSIS</span></span>
<span data-ttu-id="ceee9-103">Rimuove una credenziale da un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="ceee9-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceee9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ceee9-104">SYNTAX</span></span>

### <span data-ttu-id="ceee9-105">ObjectIdWithKeyIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ceee9-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceee9-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="ceee9-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceee9-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ceee9-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceee9-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="ceee9-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceee9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceee9-109">DESCRIPTION</span></span>
<span data-ttu-id="ceee9-110">Il cmdlet Remove-AzureRmADSpCredential può essere usato per rimuovere una chiave di credenziale da un'entità di servizio nel caso di un compromesso o come parte della scadenza del rollover della chiave di credenziale.</span><span class="sxs-lookup"><span data-stu-id="ceee9-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="ceee9-111">L'entità servizio viene identificata fornendo l'ID oggetto o il nome dell'entità servizio (SPN).</span><span class="sxs-lookup"><span data-stu-id="ceee9-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="ceee9-112">Le credenziali da rimuovere vengono identificate dall'ID chiave se una singola credenziale deve essere rimossa o con un'opzione ' tutti ' per eliminare tutte le credenziali associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="ceee9-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="ceee9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ceee9-113">EXAMPLES</span></span>

### <span data-ttu-id="ceee9-114">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ceee9-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="ceee9-115">Questo comando rimuove una chiave di credenziale da un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="ceee9-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="ceee9-116">In questo esempio, la chiave con ID "9044423a-60A3-45AC-9ab1-09534157ebb" verrà rimossa dall'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="ceee9-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="ceee9-117">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ceee9-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="ceee9-118">Questo comando rimuove una chiave di credenziale da un'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="ceee9-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="ceee9-119">In questo esempio tutte le credenziali verranno rimosse dall'entità servizio associata al nome dell'entità servizio " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="ceee9-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="ceee9-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ceee9-120">PARAMETERS</span></span>

### <span data-ttu-id="ceee9-121">-Tutti</span><span class="sxs-lookup"><span data-stu-id="ceee9-121">-All</span></span>
<span data-ttu-id="ceee9-122">Passare a rimuovere tutte le credenziali associate all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="ceee9-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceee9-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ceee9-123">-Force</span></span>
<span data-ttu-id="ceee9-124">Passare a eliminare le credenziali senza conferma.</span><span class="sxs-lookup"><span data-stu-id="ceee9-124">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceee9-125">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ceee9-125">-KeyId</span></span>
<span data-ttu-id="ceee9-126">Specifica la chiave delle credenziali da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ceee9-126">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="ceee9-127">Gli ID chiave per un'entità di servizio possono essere ottenuti usando il cmdlet Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="ceee9-127">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceee9-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ceee9-128">-ObjectId</span></span>
<span data-ttu-id="ceee9-129">ID oggetto dell'entità servizio da cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="ceee9-129">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceee9-130">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ceee9-130">-ServicePrincipalName</span></span>
<span data-ttu-id="ceee9-131">Nome (SPN) dell'entità servizio per cui rimuovere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="ceee9-131">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceee9-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ceee9-132">-Confirm</span></span>
<span data-ttu-id="ceee9-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceee9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceee9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceee9-134">-WhatIf</span></span>
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

### <span data-ttu-id="ceee9-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceee9-135">-DefaultProfile</span></span>
<span data-ttu-id="ceee9-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ceee9-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceee9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceee9-137">CommonParameters</span></span>
<span data-ttu-id="ceee9-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceee9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceee9-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceee9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceee9-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ceee9-140">INPUTS</span></span>

## <span data-ttu-id="ceee9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ceee9-141">OUTPUTS</span></span>

## <span data-ttu-id="ceee9-142">Note</span><span class="sxs-lookup"><span data-stu-id="ceee9-142">NOTES</span></span>

## <span data-ttu-id="ceee9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ceee9-143">RELATED LINKS</span></span>

[<span data-ttu-id="ceee9-144">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ceee9-144">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="ceee9-145">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="ceee9-145">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="ceee9-146">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ceee9-146">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


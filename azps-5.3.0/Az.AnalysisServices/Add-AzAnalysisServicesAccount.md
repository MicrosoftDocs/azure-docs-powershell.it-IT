---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479099"
---
# <span data-ttu-id="9be10-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="9be10-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="9be10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9be10-102">SYNOPSIS</span></span>
<span data-ttu-id="9be10-103">Aggiunge un account autenticato da usare per le richieste di cmdlet del server di Analysis Services Azure.</span><span class="sxs-lookup"><span data-stu-id="9be10-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="9be10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9be10-104">SYNTAX</span></span>

### <span data-ttu-id="9be10-105">UserParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9be10-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9be10-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9be10-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9be10-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9be10-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9be10-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9be10-108">DESCRIPTION</span></span>
<span data-ttu-id="9be10-109">Il cmdlet Add-AzAnalysisServicesAccount viene usato per accedere a un'istanza di Azure Analysis Services server</span><span class="sxs-lookup"><span data-stu-id="9be10-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="9be10-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9be10-110">EXAMPLES</span></span>

### <span data-ttu-id="9be10-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9be10-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="9be10-112">Questo esempio aggiungerà l'account specificato dalla variabile $UserCredential all'ambiente di Analysis Services westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="9be10-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="9be10-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9be10-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="9be10-114">Il primo comando ottiene le credenziali principali del servizio applicazioni e le archivia nella variabile $ApplicationCredential.</span><span class="sxs-lookup"><span data-stu-id="9be10-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="9be10-115">Il secondo comando consente di aggiungere l'account dell'entità servizio applicazione specificato dalla variabile $ApplicationCredential e ID tenant all'ambiente Analysis Services di westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="9be10-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="9be10-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9be10-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="9be10-117">Questo esempio aggiungerà l'account dell'entità servizio applicazione specificato da ApplicationId, ID tenant e CertificateThumbprint all'ambiente westcentralus.asazure.windows.net Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="9be10-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="9be10-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9be10-118">PARAMETERS</span></span>

### <span data-ttu-id="9be10-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9be10-119">-ApplicationId</span></span>
<span data-ttu-id="9be10-120">ID applicazione.</span><span class="sxs-lookup"><span data-stu-id="9be10-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be10-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="9be10-121">-CertificateThumbprint</span></span>
<span data-ttu-id="9be10-122">Hash del certificato (identificazione personale)</span><span class="sxs-lookup"><span data-stu-id="9be10-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be10-123">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="9be10-123">-Credential</span></span>
<span data-ttu-id="9be10-124">Credenziali di accesso</span><span class="sxs-lookup"><span data-stu-id="9be10-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be10-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="9be10-125">-RolloutEnvironment</span></span>
<span data-ttu-id="9be10-126">Nome dell'ambiente di Azure Analysis Services a cui eseguire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="9be10-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="9be10-127">In base al nome completo del server, ad esempio asazure://westcentralus.asazure.windows.net/testserver, il valore corretto per questa variabile sarà westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="9be10-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be10-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9be10-128">-ServicePrincipal</span></span>
<span data-ttu-id="9be10-129">Indica che l'account viene autenticato fornendo le credenziali dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9be10-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be10-130">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="9be10-130">-TenantId</span></span>
<span data-ttu-id="9be10-131">Nome del tenant o ID</span><span class="sxs-lookup"><span data-stu-id="9be10-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9be10-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9be10-132">-Confirm</span></span>
<span data-ttu-id="9be10-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9be10-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9be10-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9be10-134">-WhatIf</span></span>
<span data-ttu-id="9be10-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9be10-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9be10-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9be10-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9be10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9be10-137">CommonParameters</span></span>
<span data-ttu-id="9be10-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9be10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9be10-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9be10-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9be10-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9be10-140">INPUTS</span></span>

### <span data-ttu-id="9be10-141">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9be10-141">None</span></span>

## <span data-ttu-id="9be10-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9be10-142">OUTPUTS</span></span>

### <span data-ttu-id="9be10-143">Microsoft. Azure. Commands. AnalysisServices. dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="9be10-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="9be10-144">Note</span><span class="sxs-lookup"><span data-stu-id="9be10-144">NOTES</span></span>
<span data-ttu-id="9be10-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="9be10-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="9be10-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9be10-146">RELATED LINKS</span></span>

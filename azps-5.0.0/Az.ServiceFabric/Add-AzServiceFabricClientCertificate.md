---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200291"
---
# <span data-ttu-id="b114f-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b114f-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="b114f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b114f-102">SYNOPSIS</span></span>
<span data-ttu-id="b114f-103">Aggiungere il nome o l'identificazione personale comune al cluster per scopi di autenticazione del client.</span><span class="sxs-lookup"><span data-stu-id="b114f-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="b114f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b114f-104">SYNTAX</span></span>

### <span data-ttu-id="b114f-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="b114f-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b114f-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="b114f-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b114f-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="b114f-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b114f-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="b114f-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b114f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b114f-109">DESCRIPTION</span></span>
<span data-ttu-id="b114f-110">USA **Add-AzServiceFabricClientCertificate** per aggiungere un nome comune e un'identificazione personale dell'autorità di certificazione o certificato al cluster, in modo che il client possa usarlo per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b114f-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="b114f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b114f-111">EXAMPLES</span></span>

### <span data-ttu-id="b114f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b114f-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="b114f-113">Questo comando aggiungerà il certificato con l'identificazione personale "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" al cluster, in modo che il client possa usare il certificato come amministratore per comunicare con il cluster.</span><span class="sxs-lookup"><span data-stu-id="b114f-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="b114f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b114f-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="b114f-115">Questo comando aggiungerà un certificato client di sola lettura il cui nome comune è "Contoso.com" e l'identificazione personale dell'autorità di certificazione è "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" per il cluster.</span><span class="sxs-lookup"><span data-stu-id="b114f-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="b114f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b114f-116">PARAMETERS</span></span>

### <span data-ttu-id="b114f-117">-Amministratore</span><span class="sxs-lookup"><span data-stu-id="b114f-117">-Admin</span></span>
<span data-ttu-id="b114f-118">Tipo di autenticazione client</span><span class="sxs-lookup"><span data-stu-id="b114f-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="b114f-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="b114f-120">Specificare l'identificazione personale del certificato client che contiene solo le autorizzazioni di amministratore</span><span class="sxs-lookup"><span data-stu-id="b114f-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="b114f-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="b114f-122">Specificare il nome comune del client, l'identificazione personale dell'autorità emittente e il tipo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="b114f-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="b114f-123">-CommonName</span></span>
<span data-ttu-id="b114f-124">Specificare il nome comune del certificato client</span><span class="sxs-lookup"><span data-stu-id="b114f-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b114f-125">-DefaultProfile</span></span>
<span data-ttu-id="b114f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b114f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b114f-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="b114f-127">-IssuerThumbprint</span></span>
<span data-ttu-id="b114f-128">Specificare l'identificazione personale dell'autorità emittente del certificato client</span><span class="sxs-lookup"><span data-stu-id="b114f-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="b114f-129">-Name</span></span>
<span data-ttu-id="b114f-130">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="b114f-130">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="b114f-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="b114f-132">Specificare l'identificazione personale del certificato client che ha solo l'autorizzazione di sola lettura</span><span class="sxs-lookup"><span data-stu-id="b114f-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b114f-133">-ResourceGroupName</span></span>
<span data-ttu-id="b114f-134">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b114f-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b114f-135">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="b114f-135">-Thumbprint</span></span>
<span data-ttu-id="b114f-136">Specificare l'identificazione personale del certificato client</span><span class="sxs-lookup"><span data-stu-id="b114f-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b114f-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b114f-137">-Confirm</span></span>
<span data-ttu-id="b114f-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b114f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b114f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b114f-139">-WhatIf</span></span>
<span data-ttu-id="b114f-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b114f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b114f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b114f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b114f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b114f-142">CommonParameters</span></span>
<span data-ttu-id="b114f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b114f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b114f-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b114f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b114f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b114f-145">INPUTS</span></span>

### <span data-ttu-id="b114f-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b114f-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b114f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b114f-147">System.String</span></span>

### <span data-ttu-id="b114f-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="b114f-148">System.String[]</span></span>

### <span data-ttu-id="b114f-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="b114f-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="b114f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b114f-150">OUTPUTS</span></span>

### <span data-ttu-id="b114f-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b114f-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b114f-152">Note</span><span class="sxs-lookup"><span data-stu-id="b114f-152">NOTES</span></span>

## <span data-ttu-id="b114f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b114f-153">RELATED LINKS</span></span>

[<span data-ttu-id="b114f-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b114f-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)

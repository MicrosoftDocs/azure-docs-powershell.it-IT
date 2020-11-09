---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298008"
---
# <span data-ttu-id="4a4aa-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="4a4aa-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="4a4aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4aa-103">Modifica una password della credenziale del catalogo di dati di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="4a4aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a4aa-104">SYNTAX</span></span>

### <span data-ttu-id="4a4aa-105">SetByHostNameAndPort (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a4aa-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a4aa-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="4a4aa-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a4aa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a4aa-107">DESCRIPTION</span></span>
<span data-ttu-id="4a4aa-108">Il cmdlet Set-AzDataLakeAnalyticsCatalogCredential modifica una password delle credenziali associata a un catalogo di dati di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="4a4aa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a4aa-109">EXAMPLES</span></span>

### <span data-ttu-id="4a4aa-110">Esempio 1: modificare la password di una credenziale associata a un account</span><span class="sxs-lookup"><span data-stu-id="4a4aa-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="4a4aa-111">Questo comando imposta la password della credenziale sulla password specificata in NewPassword.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="4a4aa-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a4aa-112">PARAMETERS</span></span>

### <span data-ttu-id="4a4aa-113">-Account</span><span class="sxs-lookup"><span data-stu-id="4a4aa-113">-Account</span></span>
<span data-ttu-id="4a4aa-114">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-115">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="4a4aa-115">-Credential</span></span>
<span data-ttu-id="4a4aa-116">Specifica il nome e la password corrente delle credenziali da modificare.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4a4aa-117">-CredentialName</span></span>
<span data-ttu-id="4a4aa-118">Specifica il nome della credenziale da modificare</span><span class="sxs-lookup"><span data-stu-id="4a4aa-118">Specifies the name of the credential to modify</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="4a4aa-119">-DatabaseHost</span></span>
<span data-ttu-id="4a4aa-120">Specifica il nome host dell'origine dati esterna a cui può connettersi la credenziale in formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a4aa-121">-DatabaseName</span></span>
<span data-ttu-id="4a4aa-122">Specifica il nome del database nell'account di analisi dei dati di Lake che contiene le credenziali.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4aa-123">-DefaultProfile</span></span>
<span data-ttu-id="4a4aa-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a4aa-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a4aa-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="4a4aa-125">-NewPassword</span></span>
<span data-ttu-id="4a4aa-126">Specifica la nuova password per le credenziali</span><span class="sxs-lookup"><span data-stu-id="4a4aa-126">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="4a4aa-127">-Port</span></span>
<span data-ttu-id="4a4aa-128">Specifica il numero di porta usato per connettersi al DatabaseHost specificato usando questa credenziale.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-129">-URI</span><span class="sxs-lookup"><span data-stu-id="4a4aa-129">-Uri</span></span>
<span data-ttu-id="4a4aa-130">Specifica l'URI (Uniform Resource Identifier) completo dell'origine dati esterna a cui può connettersi la credenziale.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4aa-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a4aa-131">-Confirm</span></span>
<span data-ttu-id="4a4aa-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a4aa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a4aa-133">-WhatIf</span></span>
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

### <span data-ttu-id="4a4aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4aa-134">CommonParameters</span></span>
<span data-ttu-id="4a4aa-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4aa-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a4aa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4aa-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a4aa-137">INPUTS</span></span>

### <span data-ttu-id="4a4aa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4a4aa-138">System.String</span></span>

### <span data-ttu-id="4a4aa-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="4a4aa-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4a4aa-140">System. Uri</span><span class="sxs-lookup"><span data-stu-id="4a4aa-140">System.Uri</span></span>

### <span data-ttu-id="4a4aa-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4a4aa-141">System.Int32</span></span>

## <span data-ttu-id="4a4aa-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a4aa-142">OUTPUTS</span></span>

### <span data-ttu-id="4a4aa-143">Microsoft. Azure. Management. datalake. Analytics. Models. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="4a4aa-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="4a4aa-144">Note</span><span class="sxs-lookup"><span data-stu-id="4a4aa-144">NOTES</span></span>

## <span data-ttu-id="4a4aa-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a4aa-145">RELATED LINKS</span></span>

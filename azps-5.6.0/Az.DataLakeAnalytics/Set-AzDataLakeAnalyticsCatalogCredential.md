---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 51af3aeffe5cf75835507e78b4638270b255fb29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988244"
---
# <span data-ttu-id="da907-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="da907-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="da907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da907-102">SYNOPSIS</span></span>
<span data-ttu-id="da907-103">Modifica una password delle credenziali del catalogo di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da907-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="da907-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da907-104">SYNTAX</span></span>

### <span data-ttu-id="da907-105">SetByHostNameAndPort (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da907-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da907-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="da907-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da907-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da907-107">DESCRIPTION</span></span>
<span data-ttu-id="da907-108">Il Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifica una password delle credenziali associata a un catalogo di Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da907-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="da907-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da907-109">EXAMPLES</span></span>

### <span data-ttu-id="da907-110">Esempio 1: Modificare la password di una credenziali associata a un account</span><span class="sxs-lookup"><span data-stu-id="da907-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="da907-111">Questo comando imposta la password delle credenziali sulla password specificata in NewPassword.</span><span class="sxs-lookup"><span data-stu-id="da907-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="da907-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da907-112">PARAMETERS</span></span>

### <span data-ttu-id="da907-113">-Account</span><span class="sxs-lookup"><span data-stu-id="da907-113">-Account</span></span>
<span data-ttu-id="da907-114">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="da907-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="da907-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="da907-115">-Credential</span></span>
<span data-ttu-id="da907-116">Specifica il nome e la password corrente delle credenziali da modificare.</span><span class="sxs-lookup"><span data-stu-id="da907-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="da907-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="da907-117">-CredentialName</span></span>
<span data-ttu-id="da907-118">Specifica il nome delle credenziali da modificare</span><span class="sxs-lookup"><span data-stu-id="da907-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="da907-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="da907-119">-DatabaseHost</span></span>
<span data-ttu-id="da907-120">Specifica il nome host dell'origine dati esterna a cui le credenziali possono connettersi nel formato mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="da907-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="da907-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da907-121">-DatabaseName</span></span>
<span data-ttu-id="da907-122">Specifica il nome del database nell'account di Data Lake Analytics che contiene le credenziali.</span><span class="sxs-lookup"><span data-stu-id="da907-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="da907-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da907-123">-DefaultProfile</span></span>
<span data-ttu-id="da907-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="da907-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da907-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="da907-125">-NewPassword</span></span>
<span data-ttu-id="da907-126">Specifica la nuova password per le credenziali</span><span class="sxs-lookup"><span data-stu-id="da907-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="da907-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="da907-127">-Port</span></span>
<span data-ttu-id="da907-128">Specifica il numero di porta usato per connettersi a DatabaseHost specificato usando queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="da907-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="da907-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="da907-129">-Uri</span></span>
<span data-ttu-id="da907-130">Specifica l'URI (Uniform Resource Identifier) completo dell'origine dati esterna a cui queste credenziali possono connettersi.</span><span class="sxs-lookup"><span data-stu-id="da907-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="da907-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da907-131">-Confirm</span></span>
<span data-ttu-id="da907-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da907-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da907-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da907-133">-WhatIf</span></span>
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

### <span data-ttu-id="da907-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da907-134">CommonParameters</span></span>
<span data-ttu-id="da907-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da907-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da907-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da907-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da907-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="da907-137">INPUTS</span></span>

### <span data-ttu-id="da907-138">System.String</span><span class="sxs-lookup"><span data-stu-id="da907-138">System.String</span></span>

### <span data-ttu-id="da907-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="da907-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="da907-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="da907-140">System.Uri</span></span>

### <span data-ttu-id="da907-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="da907-141">System.Int32</span></span>

## <span data-ttu-id="da907-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da907-142">OUTPUTS</span></span>

### <span data-ttu-id="da907-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="da907-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="da907-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="da907-144">NOTES</span></span>

## <span data-ttu-id="da907-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da907-145">RELATED LINKS</span></span>
